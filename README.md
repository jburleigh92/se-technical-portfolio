# SE Technical Portfolio  
**Author:** Jason Burleigh  
**Role:** Solutions Engineer • Automation Engineer • Systems Architect  
**Focus Areas:** API integrations, automation, workflow design, multi-system orchestration, POS/eCommerce/dispatch integrations  

![GitHub followers](https://img.shields.io/github/followers/jburleigh92?style=social)
![GitHub stars](https://img.shields.io/github/stars/jburleigh92?style=social)
![Last Commit](https://img.shields.io/github/last-commit/jburleigh92/se-technical-portfolio)
![Top Language](https://img.shields.io/github/languages/top/jburleigh92/se-technical-portfolio)

---

# Table of Contents
1. [Overview](#overview)
2. [Highlighted Projects](#highlighted-projects)
3. [Project Case Studies](#project-case-studies)
   - [AutoEnrollEngine](#autoenrollengine)
   - [PostPay Automation](#postpay-automation)
   - [BakedBudz Store v1 → v2](#bakedbudz-store-v1--v2)
4. [Skill Summary](#skill-summary)
5. [Technical Strengths](#technical-strengths)
6. [How to Navigate This Portfolio](#how-to-navigate-this-portfolio)
7. [Contact](#contact)

---

# Overview
This repository is the central hub for my technical portfolio. I design and build end-to-end systems involving API integrations, workflow automation, dispatch platforms, eCommerce logic, POS systems, loyalty engines, and real-time event pipelines.

My work spans:
- event-driven architecture  
- multi-system automations  
- POS → eCommerce → dispatch integrations  
- webhook engineering  
- reverse engineering undocumented APIs  
- building high-impact operational tooling  

Every project in this portfolio is based on real production work I designed or built to support high-volume cannabis delivery and eCommerce operations.

---

# Highlighted Projects

### **1. AutoEnrollEngine**
Real-time customer verification, profile creation, opt-in sync, and SMS notifications triggered by Tookan driver “Verified Customer” events.  
**Tech:** Python, Flask, Selenium, Alpine IQ API, Tookan Webhooks  
📌 *Full case study below*

---

### **2. PostPay Automation**
A fully automated payment-ingestion + Slack notification engine parsing emails from Zelle, Venmo, Cash App, and Apple Pay to verify payments instantly.  
**Tech:** Python, SQLite, IMAP/Gmail API, Slack API  
📌 *Includes modular codebase + legacy versions folder*

---

### **3. BakedBudz Store v1 → v2**
Architected both the Blaze-powered store (v1) and the full WooCommerce rebuild (v2), solving major API and plugin limitations through custom middleware and system design.  
**Tech:** Blaze POS API, WooCommerce, WordPress, PHP, Webhooks, ID verification systems  
📌 *Complete architectural narrative included*

---

# Project Case Studies

## AutoEnrollEngine  
A multi-system automation stack that used Tookan “Verified Customer” events to trigger a fully automated workflow:

- Selenium-based ETA extraction  
- automatic customer creation  
- SMS opt-in override  
- loyalty point assignment  
- transactional outbound SMS via Alpine IQ  

This replaced Alpine’s manual UI-driven workflow and required zero dispatcher involvement.

**Repo:** https://github.com/jburleigh92/AutoEnrollEngine  
**Architecture:** `architecture/autoenrollengine-architecture.md`

---

## PostPay Automation  
A real-time payment-parsing and Slack-alerting engine used to validate 70–100+ orders/day with near-zero human involvement.

Core capabilities:
- Gmail ingestion  
- multi-parser architecture  
- duplicate-detection and audit logging  
- SQLite event log  
- Slack delivery notifications  
- automated sleep window logic  

Includes all production code + 3 generations of legacy versions.

**Repo Folder:** https://github.com/jburleigh92/PostPay  
**Codebase:** Python, SQLite, Slack API, IMAP  

---

## BakedBudz Store v1 → v2  
A complete end-to-end rebuild of a cannabis eCommerce & delivery stack.

**v1:** Blaze plugin with major limitations  
**v2:** Fully independent WooCommerce architecture with flexible API middleware, dispatch integration, catalog mapping tables, loyalty logic, and built-in tracking UI.

My responsibilities included:
- architecture design  
- API testing and validation  
- data mapping  
- developer guidance  
- webhook debugging  
- reverse engineering Blaze’s undocumented behaviors  

**Architecture:** `architecture/bakedbudz-v1-v2.md`

---

# Skill Summary

### **Languages & Frameworks**
- Python (primary)
- Flask, FastAPI  
- JavaScript / Node  
- PHP (WordPress plugin debugging)  
- SQL / SQLite  

### **APIs & Integrations**
- Blaze POS API  
- Alpine IQ API  
- Tookan Webhooks  
- Onfleet API  
- WooCommerce REST API  
- Gmail API / IMAP  
- Slack API  
- ID Verification providers  
- Payment providers (Venmo, Cash App, Zelle, etc.)

### **Areas of Expertise**
- multi-system workflow automation  
- event-driven architecture  
- webhook ingestion and transformation  
- data normalization  
- dispatch/route logistics  
- catalog and inventory sync  
- ETL-style transformations  
- reverse engineering undocumented behavior  

---

# Technical Strengths

### **Integration Design**
I excel at connecting multiple platforms together and designing the data flow between them—identifying edge cases, failure modes, and fallback logic.

### **Reverse Engineering**
Many of these systems required diagnosing undocumented APIs, third-party plugin limitations, or inconsistent webhook payloads.

### **Operational Awareness**
I design systems around real-world constraints: delivery radius, dispatch timing, verification steps, ID compliance, inventory states, and peak-volume workflows.

### **Automation & Tooling**
Several of my tools directly replaced manual dispatcher workflows, reducing operational load by 70–90%+.

---

# How to Navigate This Portfolio
The repository contains:
- `architecture/` → system diagrams and flow documents  
- `AutoEnrollEngine/` → full Python automation project  
- `PostPay/` → full modular codebase + legacy versions  
- `projects/` → case studies in markdown format  
- `samples/` → code snippets and demonstrations  

Each major project contains:
- README or case study  
- architecture diagrams  
- example payloads  
- end-to-end workflow documentation  

---

# Contact
If you’d like to discuss my work or collaborate:

**Email:** jburleigh1992@gmail.com  
**GitHub:** https://github.com/jburleigh92  
**LinkedIn:** https://www.linkedin.com/in/jason-burleigh-962903396

---

**Thank you for reviewing my portfolio.**
This repo represents real systems I’ve built, deployed, and operated end-to-end in production environments.
