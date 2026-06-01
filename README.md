# Cloud-Based-Honeypot
Multi-layer cloud honeypot integrating Suricata, Cowrie, and Wazuh to monitor and analyze real-world attack behavior. Designed to replicate SOC-style detection, correlation, and threat analysis in a controlled lab environment.

## Overview
This project implements a **multi-layer cloud-based honeypot detection system**
designed to observe and analyze real-world attack behavior against exposed
infrastructure.

The architecture combines **network intrusion detection**, **honeypot-based
deception**, and **SIEM correlation** to replicate a SOC-style monitoring pipeline.
Attack activity is observed across multiple stages including reconnaissance,
brute-force authentication attempts, command execution, and malware retrieval.

## Architecture Overview

<img width="551" height="361" alt="HoneypotFinal2 drawio" src="https://github.com/user-attachments/assets/b201439a-24db-4531-80a2-05580eb8f0a4" />

All activity was conducted in a **controlled lab environment** using infrastructure
owned by the author. Sensitive indicators have been intentionally excluded.

---

## Objectives
- Deploy a public-facing cloud honeypot to attract opportunistic attackers
- Monitor malicious activity at both the network and application layers
- Correlate IDS and honeypot telemetry in a SIEM platform
- Analyze attacker behavior and common intrusion techniques
- Practice ethical and responsible security research

---

## Technologies Used
- Linux (Ubuntu Server)
- Cloud VPS Infrastructure
- Suricata (Network Intrusion Detection System)
- Cowrie (SSH Honeypot)
- Wazuh SIEM
- Firewall logging and system hardening controls

---

## Detection Pipeline

- Technique: TCP SYN Scan
- Target: Public VPS Infrastructure
- Detection Source: Suricata IDS
- Result: Custom detection rules successfully triggered and forwarded into Wazuh SIEM

### Suricata IDS
<img width="1288" height="346" alt="IMG_0788_converted" src="https://github.com/user-attachments/assets/ae377892-61bc-4413-9cc0-0a2c53c7c289" />


### Wazuh SIEM
<img width="3417" height="702" alt="image" src="https://github.com/user-attachments/assets/8171d9b4-19e0-4e91-b5c3-ce02628b373d" />

#### Detection Validation

Controlled Nmap reconnaissance scans were performed against the VPS to validate the effectiveness of the detection pipeline. Suricata IDS successfully detected scan activity, triggered custom alert signatures, and forwarded events into Wazuh SIEM. This testing confirmed proper operation of the end-to-end monitoring architecture, including alert generation, log forwarding, and centralized analysis.

### Certain IP addresses and infrastructure identifiers have been intentionally redacted for operational security purposes.

## Results
    - 200+ attack events over 1 week
    - 10+ attacker IPs
    - 7 countries
    - Wazuh correlation
    
