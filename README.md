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

## Architecture Overview

Attacker
--> 
Suricata (Network IDS)
--> 
Cowrie (SSH Honeypot)
-->
Wazuh Agent
-->
Wazuh Manager / SIEM
