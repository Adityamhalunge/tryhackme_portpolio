# TryHackMe Write-Up: Introduction to EDR (Endpoint Detection and Response)

## Platform

**TryHackMe**

## Room Name

**Introduction to EDR**

## Category

* Security Operations Center (SOC)
* Endpoint Security
* Threat Detection
* Incident Response

---

# Objective

The objective of this room was to understand how Endpoint Detection and Response (EDR) solutions help security teams monitor, detect, investigate, and respond to advanced endpoint threats.

## Learning Objectives

During this room, I learned:

* Basics of EDR and how it works
* Difference between traditional Antivirus and EDR solutions
* Architecture of an EDR solution
* Types of endpoint telemetry collected by EDR
* Detection and response capabilities
* Practical investigation using EDR alerts

---

# What is EDR?

Endpoint Detection and Response (EDR) is a cybersecurity solution designed to continuously monitor endpoints, detect suspicious activities, investigate threats, and provide response capabilities.

EDR provides deep-level endpoint visibility and helps security teams identify malicious activities even after a threat enters the system.

Examples of EDR solutions:

* CrowdStrike Falcon
* SentinelOne ActiveEDR
* Microsoft Defender for Endpoint
* OpenEDR

---

# Traditional Antivirus vs EDR

## Antivirus

Traditional Antivirus mainly focuses on preventing known malware before execution.

Detection methods:

* Signature-based detection
* Known malware database matching

Limitations:

* Limited visibility after compromise
* Difficulty detecting advanced attacks
* Mostly prevention focused

---

## Endpoint Detection and Response (EDR)

EDR continuously monitors endpoint activities before, during, and after an attack.

EDR provides:

* Continuous monitoring
* Threat hunting
* Behavior analysis
* Incident investigation
* Response actions

Example:

If malware bypasses antivirus and executes on a system, EDR can still detect suspicious behavior through process activity, command execution, registry changes, and network connections.

---

# EDR Architecture

EDR works using endpoint agents installed on devices.

The EDR agent works like the eyes and ears of the security team.

## EDR Workflow

Endpoint
↓
EDR Agent
↓
Telemetry Collection
↓
EDR Console
↓
Detection & Investigation
↓
Response Action

The agent collects security-related data from endpoints and sends it to the centralized EDR platform for analysis.

---

# Important Features of EDR

## 1. Visibility

EDR provides deep visibility into endpoint activities.

Examples:

* Process execution
* File modifications
* Folder changes
* Registry modifications
* User activities
* Network connections

---

## 2. Detection

EDR detects threats using multiple techniques.

### Signature-Based Detection

Detects known malicious files or indicators.

Example:

Known malware hash detected on endpoint.

### Behavior-Based Detection

Detects suspicious behavior patterns.

Example:

A normal application suddenly starts PowerShell and connects to an unknown IP address.

---

## 3. Response

After detecting suspicious activity, security analysts can take response actions directly from the EDR console.

Common response actions:

* Isolate infected endpoint
* Kill malicious process
* Quarantine suspicious files
* Block malicious activity
* Start investigation

---

# Endpoint Telemetry Collection

Telemetry means security data collected from endpoints by the EDR agent.

Types of telemetry collected:

## Process Telemetry

Monitoring:

* Process creation
* Process execution
* Process termination

Example:

Suspicious PowerShell execution detected.

---

## Network Telemetry

Monitoring:

* Network connections
* External communication
* Suspicious IP connections

Example:

Endpoint communicating with attacker Command & Control server.

---

## Command Line Activity

Monitoring commands executed on endpoints.

Example:

Suspicious command:

powershell.exe -encodedcommand

Attackers commonly use encoded commands to hide malicious activity.

---

## File System Activity

Monitoring:

* File creation
* File modification
* File deletion

Example:

Malware modifying system files.

---

## Registry Activity

Monitoring Windows Registry changes.

Example:

Malware creating registry keys for persistence.

---

# Practical Lab Experience

During the practical section, I analyzed different EDR scenarios and investigated suspicious endpoint activities.

Tasks performed:

* Reviewed endpoint security alerts
* Investigated suspicious processes
* Checked telemetry information
* Analyzed user activity
* Identified malicious behavior
* Decided appropriate response actions

---

# SOC Analyst Learning Outcome

This room helped me understand how SOC analysts use EDR solutions in real-world environments.

Key SOC skills practiced:

✔ Endpoint investigation
✔ Alert analysis
✔ Threat detection concepts
✔ Incident response workflow
✔ Understanding endpoint telemetry

---

# Key Takeaways

* Antivirus focuses mainly on prevention, while EDR focuses on detection, investigation, and response.
* EDR agents continuously collect endpoint telemetry.
* Telemetry helps analysts understand attacker activity.
* Behavioral detection helps identify advanced threats.
* Response actions help contain security incidents quickly.

---

# Skills Improved

* Endpoint Security
* SOC Analysis
* Incident Response
* Threat Investigation
* EDR Fundamentals

---

Completed as part of my SOC Analyst learning journey.

