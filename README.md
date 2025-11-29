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

## 1. AutoEnrollEngine
Real-time customer verification, profile creation, opt-in sync, and SMS notifications triggered by Tookan driver “Verified Customer” events.

**Tech:** Python, Flask, Selenium, Alpine IQ API, Tookan Webhooks  
**Repository:** https://github.com/jburleigh92/AutoEnrollEngine     
**Architecture:** `architecture/AutoEnrollEngine_system_diagram`  
**Case Study:** `case-studies/AutoEnrollEngine`

---

## 2. PostPay Automation
A fully automated payment-ingestion and Slack-notification engine processing Zelle, Cash App, Venmo, and Apple Pay signals in real time.

**Tech:** Python, SQLite, Slack API, Gmail/IMAP  
**Repository:** https://github.com/jburleigh92/PostPay  
**Case Study:** `case-studies/PostPay`  
**Architecture:** `architecture/PostPay_system_diagram`

---

## 3. BakedBudz Store v1 → v2
A complete rebuild of the BakedBudz online store.

**v1:** Blaze-powered store with major plugin limitations  
**v2:** Fully custom WooCommerce rebuild with middleware, catalog mapping, loyalty features, and integrated dispatch UI.  

**Architecture:** `architecture/bakedbudz_system_diagram`  
**Case Study:** `case-studies/bakedbudz.store`  

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
Designing the data flow between multiple platforms—mapping payloads, identifying failure modes, implementing fallback logic.

### Reverse Engineering
Diagnosing undocumented APIs, plugin limitations, sandbox issues, and unexpected webhook payloads.

### Operational Awareness
Systems designed around real-world constraints: delivery radius, ID verification, dispatch timing, compliance, and peak-volume conditions.

### Automation & Tooling
Many of these tools replaced manual dispatcher workflows, reducing operational load by 70–90%.

---

# How to Navigate This Portfolio

This repository contains:

- **`architecture/`**  
  System architecture diagrams for each major project.

- **`case-studies/`**  
  Narrative project breakdowns with business context, before/after workflows, and outcomes.

- **`AutoEnrollEngine/`**  
  Full production automation project.

- **`PostPay/`**  
  Modular payment-ingestion automation (repo linked externally) + supporting case study.

- **`bakedbudz.store/`**  
  eCommerce architecture, migration logic, and solution design.

Each project folder includes:
- architecture diagram  
- full code or pseudo-code  
- workflows and payload examples  
- business impact explanation  
- system design reasoning  

---

# Contact
**Email:** jburleigh1992@gmail.com  
**GitHub:** https://github.com/jburleigh92  
**LinkedIn:** https://www.linkedin.com/in/jason-burleigh-962903396  

---

Thank you for reviewing my portfolio.  
This repository represents real systems I have designed, built, deployed, and operated in production environments.
