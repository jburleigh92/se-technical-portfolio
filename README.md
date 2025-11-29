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

Every project here is based on **real production work** supporting high-volume cannabis delivery and eCommerce operations.

---

# Highlighted Projects

## 1. PostPay Automation
A fully automated payment-ingestion and Slack-notification engine processing Zelle, Cash App, Venmo, and Apple Pay signals in real time.

**Tech:** Python, SQLite, Slack API, Gmail/IMAP  
**Repository:** https://github.com/jburleigh92/PostPay  
**Architecture:** `architecture/PostPay_system_diagram`  
**Case Study:** `case-studies/PostPay`

**Business Outcome**
- Eliminated manual dispatcher verification for ~70–100 payments/day.  
- Reduced order delays caused by “payment confirmation waiting.”  
- Created an audit log reducing disputes and lost revenue.

**Why This Matters for Solutions Engineering**
Shows ability to design a multi-system pipeline, solve operational bottlenecks, and build reliable real-time automation.

---

## 2. AutoEnrollEngine
Real-time customer verification, profile creation, opt-in sync, and SMS notifications triggered by Tookan driver “Verified Customer” events.

**Tech:** Python, Flask, Selenium, Alpine IQ API, Tookan Webhooks  
**Repository:** https://github.com/jburleigh92/AutoEnrollEngine  
**Architecture:** `architecture/AutoEnrollEngine_system_diagram`  
**Case Study:** `case-studies/AutoEnrollEngine`

**Business Outcome**
- Automatically converted “in-delivery verified customers” into full CRM profiles.  
- Increased opt-ins, loyalty attachment, and SMS deliverability.  
- Removed manual dispatcher tasks and human delays.

**Why This Matters for Solutions Engineering**
Demonstrates system orchestration, API chaining, event-triggered automation, and cross-platform workflow design.

---

## 3. BakedBudz Store v1 → v2
A complete rebuild of the BakedBudz online store.

**v1:** Blaze-powered store with significant plugin and API limitations  
**v2:** Fully custom WooCommerce architecture with middleware, catalog mapping, loyalty support, and integrated dispatch UI.

**Architecture:** `architecture/bakedbudz_system_diagram`  
**Case Study:** `case-studies/bakedbudz.store`

**Business Outcome**
- Improved conversion rates by removing Blaze plugin constraints.  
- Enabled flexible promotions, tracking UI, and API-driven inventory logic.  
- Reduced vendor dependency and enabled full ownership of the commerce stack.

**Why This Matters for Solutions Engineering**
Shows product thinking, migration design, API validation, and ability to diagnose/replace failing vendor systems.

---

# Project Case Studies
Full project narratives (problems, architecture, outcomes) are included in:

``
case-studies/
│
├── AutoEnrollEngine
├── PostPay
└── bakedbudz.store
``

Each one includes:
- before & after workflow  
- business impact  
- what was automated  
- technical architecture  
- what I specifically contributed  

---

# Skill Summary

## Languages & Frameworks
- Python  
- Flask, FastAPI  
- JavaScript / Node  
- PHP (WordPress plugin debugging)  
- SQL / SQLite  

## APIs & Integrations
- Blaze POS API  
- Alpine IQ API  
- Tookan Webhooks  
- Onfleet API  
- WooCommerce REST API  
- Slack API  
- Gmail API / IMAP  
- Payment providers (Zelle, Venmo, Cash App, Apple Cash)

## Areas of Expertise
- multi-system workflow automation  
- event-driven pipelines  
- webhook ingestion + transformation  
- catalog/inventory sync  
- ETL-style data normalization  
- reverse engineering undocumented APIs  

---

# Technical Strengths

### Integration Design
Designing clean, predictable data flows between multiple platforms—mapping payloads, identifying failure modes, and creating fallback logic.

### Reverse Engineering
Diagnosing undocumented APIs, plugin limitations, sandbox mismatch behavior, and inconsistent webhook payloads.

### Operational Awareness
Systems designed with real-world constraints: delivery radius, ID verification, compliance, dispatch timing, and peak-volume behavior.

### Automation & Tooling
Many of these tools replaced manual dispatcher workflows, reducing operational workload by **70–90%**.

---

# How to Navigate This Portfolio

This repository contains:

- **`architecture/`**  
  System architecture diagrams for each major project.

- **`case-studies/`**  
  Narrative project breakdowns with before/after workflows, systems, and business outcomes.

- **`AutoEnrollEngine/`**  
  Full production automation project.

- **`PostPay/`**  
  External repo containing the modular payment-ingestion engine.

- **`bakedbudz.store/`**  
  Solution design, architecture, and migration notes.

Each project folder includes:
- architecture diagram  
- workflows & technical reasoning  
- business impact  
- code or implementation details  

---

# Contact
**Email:** jburleigh1992@gmail.com  
**GitHub:** https://github.com/jburleigh92  
**LinkedIn:** https://www.linkedin.com/in/jason-burleigh-962903396  

---

Thank you for reviewing my portfolio.  
This repository represents real systems I’ve designed, built, deployed, and operated in production environments.
