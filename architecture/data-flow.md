# Data Flow Overview — End-to-End Operational Pipeline

This document breaks down the *exact data flow* across every system in the Baked Budz delivery platform.  
It follows a single real order from:

1. **Order creation**  
2. **Customer verification**  
3. **Dispatch assignment**  
4. **Driver tracking**  
5. **Payment verification**  
6. **Loyalty enrollment**  
7. **Notifications & system outputs**

This is the **A→Z lifecycle** of every delivery.

---

# 1. Order Creation → Blaze POS

### Sources of Orders
```
Weedmaps → WM API → Blaze
BakedBudz.store v1 → Blaze Store Plugin → Blaze
BakedBudz.store v2 → Custom API → Blaze
Direct SMS → Dispatcher enters manually → Blaze
```

### Data Mapped to Blaze:
- customer_name  
- phone_number  
- delivery_address  
- cart_items / SKUs  
- subtotal / taxes / discounts  
- payment_type (unverified)  
- order_id (Blaze)  

### Blaze → Webhook Output
When Blaze creates the order, it emits:

```json
{
  "event": "order.created",
  "order_id": "123456",
  "customer": {
    "name": "John Doe",
    "phone": "8185551212"
  }
}
```

**Flow continues to verification.**

---

# 2. Blaze → Customer Verification Logic

### Script evaluates:
- returning vs new customer  
- ID on file?  
- ID expiration?  
- age check (21+)  
- duplicate orders  
- fraud patterns  

### Output Decision Tree:

```
IF fully verified → proceed to Tookan  
IF missing data → request ID upload → halt dispatch  
IF flagged → cancel or manual review
```

---

# 3. Verification → Tookan Dispatch

When verified, the script (or dispatcher in early versions) pushes the order to Tookan:

### Data sent to Tookan:
```json
{
  "job_id": "123456",
  "customer_name": "John Doe",
  "address": "...",
  "phone": "8185551212",
  "job_description": "Order #123456 — 3 items",
  "order_amount": 87.45
}
```

### Tookan returns a tracking link:
```
https://tracking.tookanapp.com/?id=ABCD1234
```

This link is used later by the WH-Listener for ETA scraping (early version) or event reading.

---

# 4. Tookan → Real-Time Driver Events

### Tookan emits webhook events such as:
```
TASK_STARTED  
REACHED_STORE  
VERIFIED_CUSTOMER  
ON_THE_WAY  
DELIVERED  
```

### Example webhook payload:
```json
{
  "event": "VERIFIED_CUSTOMER",
  "task_id": "TK123",
  "customer_phone": "8185551212",
  "tracking_link": "https://tracking.tookanapp.com/?id=ABCD1234"
}
```

This webhook is the **trigger** for loyalty automation.

---

# 5. Payment Verification — PostPay Engine

This subsystem merges **email APIs**, **SMS DB parsing**, and **Slack notifications**.

### 5.1 Email Path (Gmail API)
Services:
- Cash App  
- Venmo  
- Zelle (sometimes delayed email)

Flow:
```
Email → Gmail API → Python Parser → Extracted Payment Object → Database
```

### 5.2 SMS Path (iMessage Database Parsing)

Especially required for Zelle (real-time SMS even when email is delayed):

```
macOS chat.db → SQLite query → Extract new messages → Regex parse → Payment Object → Database
```

### 5.3 Final Output to Slack

Once payment is matched to order:

```json
{
  "status": "verified",
  "order_id": "123456",
  "amount": 87.45,
  "method": "Zelle",
  "customer": "John Doe"
}
```

Slack message example:

```
💸 PAYMENT VERIFIED  
Order #123456  
$87.45 via Zelle  
Customer: John Doe  
Driver may proceed.
```

---

# 6. Loyalty Enrollment — Tookan → Alpine IQ

Tookan’s *VERIFIED_CUSTOMER* event triggers:

### Flow:
```
Tookan Webhook → WH-Listener → Alpine API  
• Create/Lookup customer  
• Auto-enroll  
• Apply earned points  
• Send SMS  
```

### Example Alpine API call:
```http
PUT /api/v2/optin/text/8185551212/true
```

### SMS sent via Alpine API:
```
“You've been enrolled in Baked Budz Rewards!  
Your points from today’s order: 87 pts.”
```

---

# 7. Final Notifications

Every critical event flows into Slack:

```
Order Created
Customer Verified
Driver Assigned
Payment Verified
Loyalty Enrollment Complete
Errors / Alerts / Retries
```

Slack becomes the real-time control center for operations.

---

# End of `data-flow.md`

