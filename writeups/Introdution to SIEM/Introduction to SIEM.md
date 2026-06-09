# TryHackMe Write-Up: Introduction to SIEM (Security Information and Event Management)

## Platform

**TryHackMe**

## Room Name

**Introduction to SIEM**

## Category

* Security Operations Center (SOC)
* Log Analysis
* Threat Detection
* Incident Response

---

# Objective

The objective of this room was to understand how SIEM solutions collect, process, analyze, and correlate logs from different sources to detect security threats.

## Learning Objectives

During this room, I learned:

* Different types of log sources
* Limitations of working with isolated logs
* Importance of SIEM solutions in cybersecurity
* Features and capabilities of SIEM platforms
* Log collection and ingestion methods
* How SIEM alerts are generated
* Basics of alert analysis workflow

---

# What is SIEM?

SIEM stands for **Security Information and Event Management**.

A SIEM solution collects security logs from multiple sources, stores them centrally, analyzes activities, and helps security analysts detect suspicious behavior.

SIEM provides security teams with:

* Centralized visibility
* Threat detection
* Alert generation
* Investigation capability
* Incident response support

---

# Why Do We Need SIEM?

Organizations have multiple devices generating security logs:

Examples:

* Servers
* Workstations
* Firewalls
* Applications
* Authentication systems
* Network devices

Analyzing every device separately is difficult.

Problems with isolated logs:

* Time-consuming investigation
* Difficult to find relationships between events
* Limited visibility
* Delayed threat detection

SIEM solves this problem by collecting all logs into one centralized platform.

---

# Types of Log Sources

Logs collected by SIEM are mainly divided into two categories:

---

## 1. Host-Centric Logs

Host-centric logs are generated from individual systems/endpoints.

Examples:

* Windows Event Logs
* Linux Logs
* Process Activity
* User Login Events
* File Changes

Security use cases:

* Detect suspicious login attempts
* Identify malware execution
* Monitor user activities

Example:

Multiple failed login attempts from a user account.

---

## 2. Network-Centric Logs

Network-centric logs provide information about network communication.

Examples:

* Firewall Logs
* Proxy Logs
* IDS/IPS Logs
* Network Traffic Logs

Security use cases:

* Detect malicious IP communication
* Identify suspicious traffic
* Monitor data transfer

Example:

A system communicating with a known malicious IP address.

---

# Features of SIEM

## 1. Centralized Log Collection

SIEM collects logs from multiple sources and stores them in one location.

Benefits:

* Easier monitoring
* Faster investigation
* Better visibility

---

## 2. Log Normalization

Normalization means converting logs from different sources into a common and consistent format.

Example:

Different devices may record login events differently.

After normalization, SIEM converts them into a standard format that can be easily analyzed.

Benefits:

* Easier searching
* Faster analysis
* Better correlation

---

## 3. Log Correlation

Correlation is the process of finding relationships between logs from different sources.

Example:

Firewall Log:

```
Connection from suspicious IP detected
```

Endpoint Log:

```
Malicious file executed
```

SIEM correlates these events and identifies possible compromise.

---

# Log Ingestion Methods

SIEM collects logs using different ingestion techniques.

---

## 1. Agent / Forwarder

A lightweight agent is installed on the endpoint.

The agent collects logs and forwards them to the SIEM.

Example:

Endpoint → Forwarder → SIEM

---

## 2. Syslog

Syslog is commonly used by network devices to send logs.

Examples:

* Firewall
* Router
* Linux Server

Flow:

Device → Syslog → SIEM

---

## 3. Manual Upload

Security analysts can manually upload log files into SIEM for analysis.

Example:

Uploading exported log files during investigation.

---

## 4. Port Forwarding

SIEM receives logs through configured network ports.

Devices send events directly to the SIEM listener.

---

# How SIEM Alerts are Triggered

SIEM detects threats using detection rules and correlation logic.

Process:

Log Sources
↓
Log Collection
↓
Normalization
↓
Correlation
↓
Detection Rules
↓
Security Alert

Detection rules continuously check logs for suspicious activities.

---

# Example SIEM Detection Scenario

Attack Scenario:

An attacker attempts brute force login.

Collected Logs:

Authentication Logs:

* Multiple failed login attempts

Network Logs:

* Same external IP repeatedly connecting

SIEM Correlation:

Multiple failed logins + suspicious IP activity

Triggered Alert:

"Possible Brute Force Attack Detected"

SOC Analyst Action:

* Analyze alert details
* Check affected user
* Review source IP
* Escalate or respond

---

# Practical Lab Experience

During this room, I explored SIEM concepts and understood:

* How logs are collected
* How SIEM processes security events
* How correlation works
* How alerts are generated
* How SOC analysts investigate suspicious activity

---

# SOC Analyst Learning Outcome

Skills practiced:

✔ Log Analysis
✔ SIEM Fundamentals
✔ Alert Investigation
✔ Security Monitoring
✔ Detection Engineering Basics

---

# Key Takeaways

* SIEM provides centralized security monitoring.
* Logs from different sources provide better visibility.
* Normalization converts logs into a common format.
* Correlation helps identify attack patterns.
* Detection rules generate alerts for suspicious activities.
* SIEM is a core technology used by SOC analysts.

---

Completed as part of my SOC Analyst learning journey.

