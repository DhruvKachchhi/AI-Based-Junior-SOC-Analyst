# 🛡️ AI-Based Junior SOC Analyst

> **Automated Network Threat Detection & AI-Driven SOC Triage using Python, Tshark, and Airia AI**

![Lab Architecture](screenshots/01-Lab-Architecture.png)

---

## 📖 Project Overview

AI-Based Junior SOC Analyst is a cybersecurity automation project that simulates the workflow of a Tier-1 Security Operations Center (SOC) analyst.

The solution captures live network traffic using **TShark**, analyzes packet activity with **Python**, detects suspicious network behavior based on configurable thresholds, generates structured JSON alerts, and submits them to an **AI-powered SOC Analyst** built using **Airia AI**.

The AI agent performs automated threat triage using a custom SOC playbook and returns:

- Threat Classification
- Risk Score
- Confidence Level
- MITRE ATT&CK Mapping
- Recommended Analyst Actions
- Executive Summary

This project demonstrates how AI can assist SOC analysts by automating the initial investigation and triage of network security alerts.

---

## 🚀 Key Features

- Live network traffic capture using TShark
- Automated packet analysis using Python
- Threshold-based anomaly detection
- Automatic JSON alert generation
- REST API integration with Airia AI
- AI-powered SOC alert triage
- MITRE ATT&CK framework mapping
- Risk scoring and confidence assessment
- Executive-level incident summary

---

## 🏗️ Lab Architecture

![Lab Architecture](screenshots/01-Lab-Architecture.png)

---

## 🔄 Project Workflow

1. Ubuntu generates ICMP network traffic.
2. Kali Linux captures traffic using TShark.
3. Python converts captured packets into CSV format.
4. Network traffic is analyzed based on packet thresholds.
5. A structured JSON alert is generated for suspicious activity.
6. The alert is sent to Airia AI through the REST API.
7. Airia AI performs automated SOC triage using a custom playbook.
8. A structured security assessment is returned with recommendations.

---

## 🖥️ Lab Environment

| Component | Purpose |
|-----------|---------|
| Ubuntu Linux | Traffic Generator |
| Kali Linux | Packet Capture & Traffic Analysis |
| Python | Automation & Detection Logic |
| TShark | Packet Capture |
| Airia AI | AI-Based SOC Triage |
| REST API | Alert Submission |

---

## ⚙️ Technologies Used

- Python 3
- TShark
- Wireshark
- Kali Linux
- Ubuntu Linux
- VirtualBox
- Airia AI
- REST API
- JSON
- MITRE ATT&CK Framework
