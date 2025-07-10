# Proposal: Qubic Alert System (QAS)  
**Request:** 18.6 Billion QUBIC priced at ~1,320 USDT per Billion  
**Receiving Wallet:** `MODMHIDMLHWBGHKQZYDIRMICOVRAAXCLXWJVEMTSQDIFAIEZKLBQXIGDNZJN`  
**Submitted by:** PicklePixel  
**Date:** 07/02/2025  

## Decision  
> _Option 1: Yes, approve funding._  
> _Option 0: No, I don't want._


## Summary

This proposal seeks funding to launch the **Qubic Alert System (QAS)** a real-time alerting platform for wallet activity in the Qubic ecosystem. Initially offering email deposit notifications, QAS will evolve into a modular, multi-channel system supporting Telegram, Discord, SMS, and developer APIs. The platform improves visibility into wallet transactions, removing the need to manually refresh QXExplorer during reward distribution periods. By decoding transaction data directly from the backend, QAS enables faster and more reliable detection of deposits than the existing frontend.

> _The current MVP delivers email alerts, but the long-term roadmap transforms QAS into a full alerting and developer integration suite for the Qubic network._

## Problem

Today, Qubic users especially miners and active participants — are forced to manually monitor their wallets during reward distribution periods by refreshing QXExplorer. This process is inefficient, error-prone, and often delayed due to frontend caching and network congestion.

There is currently no system-wide mechanism to notify users of incoming or outgoing transactions in real time. As a result:
- Rewards may appear late or be missed entirely
- Users are left guessing whether payouts have occurred
- There is no visibility into overall wallet health or portfolio change
- Power users and developers lack API-accessible hooks for automation

This gap not only reduces trust in Qubic’s UX but creates unnecessary frustration and slows community participation.


## Solution

QAS monitors a wallet in real-time and sends an instant email alert when a deposit is received. By parsing lower-level data from QXExplorer’s backend response structure, the system bypasses frontend caching delays and confirms incoming transactions faster than any current method. The MVP is live and working reliably in a personal testing environment.

### Core Features (Phase 1 - MVP Complete)

- Real-time email notifications on wallet deposits
- Fast detection via backend decoding
- Simple user enrollment (wallet + email)
- Configurable polling interval and secure SMTP delivery

## Visual Demo

Below are real screenshots from the current version of QAS, showing the user experience and backend logic in action.

### 📥 Sign-Up Page (User enters Wallet + Email)

![Sign-Up UI](https://github.com/user-attachments/assets/1b14cfde-e094-48ae-9c4e-bb7c6c375edb)


---

### 📧 Subscription Confirmation Email

![Subscription Confirmation](https://github.com/user-attachments/assets/475bbb0c-fb14-4f56-a717-a87fc7431666)


---

### 💸 Deposit Alert Email Example

![Deposit Alert Email](https://github.com/user-attachments/assets/afe60583-3ec4-4ce3-a1a2-5c867709a5c4)


---

### 🖥️ Console Output (Transaction Polling Logs)

![Console Logs](https://github.com/user-attachments/assets/bc0d39cc-9450-4c90-a0b1-a01455d765c9)

## Technical Overview

QAS pulls and decodes raw transaction data directly from QXExplorer’s backend API layer. It compares wallet balance states and flags any positive changes. A custom parser filters false positives and inconsistencies. Notifications are sent through a secure email delivery system with configurable intervals, error handling, and built-in rate limiting. The system is lightweight, efficient, and designed to scale.

## Value to Qubic

- Saves users hours of manual checking
- Reduces confusion and increases trust in the reward system
- Adds professional-grade tooling to the ecosystem
- Encourages participation by improving feedback and UX
- Enables future integrations across platforms

## Roadmap

**Current Status:** ~30% complete (MVP working, backend logic tested and live)

### Phase 1: Production Launch (Post-Funding)
- Harden backend for uptime, stability, and latency reduction
- Finalize web-based UI and user configuration panel
- Add support for monitoring multiple wallets per user
- Improve polling efficiency with adaptive intervals
- Launch public-facing version with onboarding documentation

### Phase 2: Feature Expansion
- Add Telegram, Discord, and Webhook notifications
- Integrate optional SMS alerts
- Provide a real-time status dashboard with balance & payout tracking
- Introduce real-time stock and token price feeds into alerts
- Allow custom threshold triggers (e.g. "Alert me on +1000 QUBIC")

### Phase 3: Ecosystem Expansion & Developer Integration
- Launch an authenticated API endpoint for developers to access wallet event data
- Add support for multi-pool integration to track deposits from various mining sources
- Build a modular notification engine to support new channels quickly (e.g. Matrix, Signal)
- Create public-facing system status and wallet monitoring dashboards
- Design a lightweight admin panel for user/device management and usage metrics
- Add JSON/CSV export options for power users who want to analyze alerts historically

## 👥 Team

The QAS project is led by experienced contributors with deep backgrounds in blockchain infrastructure, software engineering, and distributed systems:

### 💻 PicklePixel – Co-Lead | Software Engineer
PicklePixel is the core developer behind QAS. A seasoned software engineer with a focus on blockchain, DevOps, and distributed systems, he is responsible for the backend infrastructure, wallet monitoring engine, alerting logic, and frontend delivery system. The current MVP of QAS was built and tested by PicklePixel, laying the foundation for a scalable, real-time wallet notification tool for the Qubic ecosystem.

### 🧭 ElNonito92 – Co-Lead | Product Manager 
ElNonito92 serves as strategic lead for QAS. He brings extensive experience from his current role at Ripple, where he oversees the development of microservices architecture in high-performance financial environments. With a strong engineering background and program oversight expertise, ElNonito ensures QAS is executed with production-grade reliability and a user-focused roadmap.

Together, the team combines enterprise-level planning with hands-on engineering execution, ensuring QAS is delivered efficiently and to the highest technical standards.



## QAS Project Timeline – 3-Month Roadmap

---

### 🟢 Month 1 – Phase 1: Production Launch (MVP Email Notifications)

**Week 1**  
- Transition MVP to secure staging  
- Set up production infrastructure (SSL, SMTP, monitoring)

**Week 2**  
- Finalize wallet polling logic  
- Optimize latency and handle edge cases

**Week 3**  
- Build front-end sign-up UI  
- Implement multi-wallet tracking per user

**Week 4**  
- Internal beta testing with real users  
- Gather feedback and stabilize platform

---

### 🔵 Month 2 – Phase 2: Channel Expansion & User Tools

**Week 5**  
- Integrate Telegram, Discord, and Webhook notifications  
- Begin Telegram bot integration for inline alerts

**Week 6**  
- Add SMS alert delivery  
- Implement custom threshold triggers (e.g., "Alert me if deposit > 1,000 QUBIC")

**Week 7**  
- Launch user dashboard with alert history  
- Add live wallet status overview

**Week 8**  
- Public beta launch  
- Publish full onboarding documentation

---

### 🟣 Month 3 – Phase 3: Developer Access & Ecosystem Integration

**Week 9**  
- Launch authenticated API endpoint for developer access  
- Enable key-based webhook configuration

**Week 10**  
- Support multi-pool deposit source tagging  
- Add per-source transaction labeling

**Week 11**  
- Build analytics dashboard (usage, wallets, alerts)  
- Enable CSV/JSON export for advanced users

**Week 12**  
- Final QA and polish  
- Public release and developer outreach campaign

---

### 🟠 Phase 3B (Planned Extension): Wallet Intelligence & Portfolio Alerts

> *This phase will begin after the core system is live and stable.*

- Add **outgoing transaction alerts**
- Enable **real-time portfolio value tracking** using QUBIC price feeds
- Support **custom triggers** based on wallet value change (e.g. % loss/gain)
- Deliver **daily/weekly wallet performance summaries** via email or Telegram
- Build **portfolio trend visualizations** and historical views


## 💸 Expense Breakdown

| **Category**             | **Description**                                                                 |
|--------------------------|----------------------------------------------------------------------------------|
| 🧑‍💻 Development & Engineering | - Core developer compensation  <br> - Project lead & oversight  <br> - Optional full-stack hire for dashboard/API work |
| 🏗️ Infrastructure & Operations | - High-performance server (dedicated CPU, SSD)  <br> - Managed database with backups <br> - Scalable object storage |
| ✉️ Communication & Delivery   | - Transactional email provider (high deliverability)  <br> - SMS infrastructure for global alerts <br> - Message queueing & delivery management |
| 🌐 Web & Monitoring           | - Domain name and DNS hosting  <br> - SSL/TLS certificates <br> - Uptime and health monitoring tools |
| 📊 Observability & Reliability | - Logging and metrics infrastructure  <br> - Error tracking and alerts <br> - Backup systems and security checks |
| 🧾 Administrative & Misc.     | - CI/CD pipelines and deployment tooling <br> - Code repo management and documentation  <br> - Community support resources |


## Source Code and Licensing

The code will be released under a permissive open-source license (MIT or Apache) after production launch. Sensitive logic (wallet monitoring parser and backend) will be fully documented and maintainable. If the proposal is not approved, the system will remain private and may be monetized.

## Final Notes

QAS is built to solve a frustrating, widely felt issue in the Qubic ecosystem: visibility into wallet activity. With this proposal, I will deliver a polished, production-ready alerting service that improves user experience, reduces confusion, and strengthens confidence in Qubic's reward infrastructure. The MVP is already working this proposal ensures it reaches the entire community.
