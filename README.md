# Suspicious-Behavior-Detection-Lab-using-Splunk
# 🔍 Suspicious Behavior Detection Lab using Splunk

This lab simulates real-world adversary techniques across authentication, process execution, network activity, and persistence — using **Windows logs, Sysmon**, and **Splunk**. Each detection is mapped to the [MITRE ATT&CK](https://attack.mitre.org/) framework for better visibility and threat modeling.

---

## 🎯 Goal

To simulate attacker behaviors and build Splunk detections that can help SOC analysts identify early indicators of compromise based on Windows and Sysmon log telemetry.

---

## 🧰 Tools Used

- 💾 **Windows 10 VM (target)**
- 🐚 **Sysmon (configured with SwiftOnSecurity config)**
- 📊 **Splunk (log ingestion and detection queries)**
- 🧠 **MITRE ATT&CK** (tactic and technique mapping)

---

## 📘 Detection Categories

### 🛡️ Authentication & Access

| Detection Scenario | MITRE Technique ID | Technique Name | Tactic |
|--------------------|--------------------|----------------|--------|
| Multiple failed login attempts | [T1110](https://attack.mitre.org/techniques/T1110/) | Brute Force | Credential Access |
| Successful login after several failures | [T1078](https://attack.mitre.org/techniques/T1078/) | Valid Accounts | Persistence / Defense Evasion |

---

### ⚙️ Process Execution & Behavior

| Detection Scenario | MITRE Technique ID | Technique Name | Tactic |
|--------------------|--------------------|----------------|--------|
| PowerShell with encoded command | [T1059.001](https://attack.mitre.org/techniques/T1059/001/) | PowerShell | Execution |
| Office app spawning PowerShell | [T1059.005](https://attack.mitre.org/techniques/T1059/005/) | Visual Basic | Execution |

---

### 🌐 Network Activity

| Detection Scenario | MITRE Technique ID | Technique Name | Tactic |
|--------------------|--------------------|----------------|--------|
| PowerShell making outbound connections | [T1043](https://attack.mitre.org/techniques/T1043/) | Commonly Used Port | Command and Control |
| Verification using Sysmon Event ID 3 | [T1071.001](https://attack.mitre.org/techniques/T1071/001/) | Web Protocols | Command and Control |

---

### 🛠️ Persistence & System Changes

| Detection Scenario | MITRE Technique ID | Technique Name | Tactic |
|--------------------|--------------------|----------------|--------|
| New service created on system | [T1543.003](https://attack.mitre.org/techniques/T1543/003/) | Windows Service | Persistence |
| Registry Run Key modification | [T1547.001](https://attack.mitre.org/techniques/T1547/001/) | Registry Run Keys / Startup Folder | Persistence |

---

## 📂 Lab Walkthrough

Each folder contains:
- ✔️ Event generation steps (manual or simulated)
- 🧠 SPL detection queries used in Splunk
- 📸 Screenshots of triggered events
- 🔎 Analysis of why the detection matters and how it maps to MITRE

---

## 🚀 Why This Matters

Understanding attacker techniques — not just indicators — is critical for SOC analysts. This lab builds muscle memory around:
- Writing Splunk queries for behavior-based detection
- Interpreting Windows and Sysmon logs
- Using MITRE ATT&CK as a guide for threat coverage
- Bridging red and blue team thinking


