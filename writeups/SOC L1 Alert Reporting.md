# Room: SOC L1 Alert Reporting — TryHackMe

**Difficulty:** Easy
**Category:** SOC (Security Operations Center)
**Date Completed:** 07/06/2026
**Platform:** TryHackMe

---

## 🎯 Objectives
1. Understand SOC alerts, reporting and escalation
2. How to write alert comments or case reports properly
3. How to escalate alerts to the next level
4. Apply knowledge to triage alerts

---

## 📚 What I Learned

### 1️⃣ How Alert Filtering Works

Alerts in SOC L1 are handled in two ways:

| Alert Type | What It Means | Action Taken |
|------------|--------------|--------------|
| **False Positive** | Alert triggered but no real threat | Filtered and closed by SOC L1 |
| **True Positive** | Alert is a real threat | Escalated to SOC L2 |

---

### 2️⃣ How to Write a Proper Report (The 5 W's)

Every alert report must answer these 5 questions:

| W | Question | Example |
|---|----------|---------|
| **Who** | Which user logged in, ran commands or downloaded something suspicious? | User: john.doe |
| **What** | What exactly happened? | Downloaded a malicious file |
| **When** | When did the suspicious activity start and end? | 07/06/2026 — 10:00 AM to 10:15 AM |
| **Where** | Which IP, device or website was involved? | IP: 192.168.1.10, Site: malicious.com |
| **Why** | What is your final verdict and reasoning? | Flagged as True Positive — user visited known malware domain |

---

### 3️⃣ Escalation Guide
Alert Comes In
↓
SOC L1 Investigates
↓
Is it suspicious or True Positive?
/          
YES            NO
↓              ↓
Escalate        Close Alert
to SOC L2      (False Positive)
↓
L2 Investigates Deeper
/          
Serious?       Not Serious?
↓                ↓
Escalate          Close Alert
to IR Team
