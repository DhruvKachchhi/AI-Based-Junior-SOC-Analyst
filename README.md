# 🛡️ AI-Based Junior SOC Analyst

> **Automated Network Threat Detection & AI-Driven SOC Triage using Python, TShark, and Airia AI**

![Lab Architecture](screenshots/01-Lab-Architecture.png)

<p align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Linux](https://img.shields.io/badge/Linux-Ubuntu%20%7C%20Kali-orange?logo=linux)
![TShark](https://img.shields.io/badge/TShark-Network%20Analysis-green)
![Airia AI](https://img.shields.io/badge/Airia-AI%20Powered-purple)
![Status](https://img.shields.io/badge/Status-Completed-success)

</p>

---

# 📖 Project Overview

Modern Security Operations Centers (SOCs) process thousands of security alerts every day, making rapid and accurate triage essential. This project demonstrates how Artificial Intelligence can automate the initial investigation of network security events, helping analysts prioritize alerts and reduce manual effort.

**AI-Based Junior SOC Analyst** is an end-to-end cybersecurity automation project that simulates the workflow of a Tier-1 SOC analyst. The solution captures live network traffic using **TShark**, analyzes packet activity with a custom **Python** automation script, detects suspicious network behavior based on configurable thresholds, generates structured **JSON** alerts, and submits them to an **AI-powered SOC Analyst** built on **Airia AI**.

The AI agent follows a custom SOC playbook to automatically analyze the alert, classify the threat, calculate a risk score, map the activity to the **MITRE ATT&CK Framework**, recommend appropriate analyst actions, and generate an executive summary.

This project demonstrates the integration of **Network Security**, **Python Automation**, **Packet Analysis**, **REST APIs**, and **Artificial Intelligence** to build an intelligent SOC workflow that reduces manual analysis while improving the speed and consistency of security investigations.

---

## 🎯 Project Objectives

- Capture live network traffic using TShark.
- Analyze packet activity using Python automation.
- Detect suspicious network behavior based on configurable thresholds.
- Generate structured JSON security alerts automatically.
- Integrate with Airia AI through its REST API.
- Automate SOC alert triage using a custom SOC playbook.
- Provide risk scoring, MITRE ATT&CK mapping, and recommended analyst actions.
- Demonstrate how AI can support Tier-1 SOC analysts during incident triage.


---

# ✨ Key Features

- 📡 **Live Network Traffic Capture** using TShark for real-time packet collection.
- 🐍 **Python-Based Automation** to analyze captured traffic and identify suspicious network activity.
- 📊 **Threshold-Based Detection Logic** to detect abnormal packet volume from source IP addresses.
- 📄 **Automatic JSON Alert Generation** containing structured security event information.
- 🤖 **AI-Powered SOC Triage** using Airia AI and a custom SOC playbook.
- 🎯 **Threat Classification** based on structured alert data.
- 📈 **Risk Scoring & Confidence Assessment** for prioritizing security incidents.
- 🛡️ **MITRE ATT&CK Mapping** to align detected activity with industry-standard attack techniques.
- 📋 **Automated Analyst Recommendations** to assist Tier-1 SOC analysts during investigations.
- 🔗 **REST API Integration** for seamless communication between Python automation and Airia AI.
- 💻 **Virtual Lab Environment** built using Ubuntu and Kali Linux.
- 📦 **Modular Design** allowing the detection logic and AI playbook to be easily extended.

---



# 🛠️ Technology Stack

| Category | Technology |
|----------|------------|
| Programming Language | Python 3 |
| Operating Systems | Ubuntu Linux, Kali Linux |
| Network Analysis | TShark, Wireshark |
| Virtualization | Oracle VirtualBox |
| Network Protocol | ICMP |
| Data Format | JSON, CSV, PCAP |
| AI Platform | Airia AI |
| API Communication | REST API |
| Security Framework | MITRE ATT&CK Framework |
| Detection Method | Threshold-Based Packet Analysis |
| Version Control | Git & GitHub |


---


# 🖥️ Lab Environment

The project was implemented in a virtualized cybersecurity lab to simulate a real-world Security Operations Center (SOC) workflow. Ubuntu Linux was used to generate network traffic, while Kali Linux acted as the monitoring server responsible for packet capture, traffic analysis, alert generation, and AI-powered threat triage.

| Component | Description |
|-----------|-------------|
| Host Machine | Windows 11 |
| Virtualization Platform | Oracle VirtualBox |
| Traffic Generator | Ubuntu Linux |
| Monitoring Server | Kali Linux |
| Packet Capture Tool | TShark |
| Programming Language | Python 3 |
| AI Platform | Airia AI |
| Communication Method | REST API |
| Detection Logic | Threshold-Based Packet Analysis |
| Alert Format | JSON |
| Captured Traffic | ICMP |

### Lab Topology

| Source | Destination | Purpose |
|---------|-------------|---------|
| Ubuntu Linux | Kali Linux | Generate ICMP traffic for analysis |
| Kali Linux | Airia AI | Submit generated alerts through REST API |
| Airia AI | Kali Linux | Return automated SOC triage report |

This isolated virtual lab provides a safe environment to simulate network activity, analyze captured packets, automate alert generation, and evaluate AI-assisted SOC investigations without affecting production systems.

---

# ⚙️ Project Workflow

The following workflow illustrates the complete automation pipeline implemented in this project, from network traffic generation to AI-powered SOC analysis.

### Step 1 — Network Traffic Generation

Ubuntu Linux generates ICMP traffic towards the Kali Linux monitoring server to simulate network activity within the lab environment.

### Step 2 — Packet Capture

The Python automation script initiates **TShark** to capture live network traffic on the monitoring interface for a configurable duration.

### Step 3 — Traffic Conversion

The captured **PCAP** file is automatically converted into **CSV** format using TShark, making the captured packet data easier to process programmatically.

### Step 4 — Traffic Analysis

The Python script analyzes the captured traffic by counting packets from each source IP address. If the packet count exceeds the configured threshold, the source IP is flagged as suspicious.

### Step 5 — Alert Generation

A structured JSON alert is automatically generated containing essential security information, including:

- Alert ID
- Alert Type
- Indicator Type
- Source IP Address
- Destination Host
- Destination IP Address
- Packet Count
- Capture Duration
- Data Source

### Step 6 — AI-Powered SOC Triage

The generated alert is submitted to **Airia AI** through its REST API. A custom SOC playbook validates the alert, analyzes the provided evidence, calculates a risk score, maps the activity to the MITRE ATT&CK Framework, recommends analyst actions, and generates an executive summary.

### Step 7 — Analyst Output

The final SOC triage report is returned to the monitoring server, providing actionable insights that assist a Tier-1 SOC analyst in making faster and more consistent security decisions.

### Workflow Summary

```text
Ubuntu Linux
(Traffic Generator)
        │
        ▼
ICMP Network Traffic
        │
        ▼
Kali Linux
(Packet Monitoring Server)
        │
        ▼
TShark Packet Capture
        │
        ▼
Python Traffic Analysis
        │
        ▼
Threshold-Based Detection
        │
        ▼
JSON Alert Generation
        │
        ▼
Airia AI REST API
        │
        ▼
SOC Playbook Execution
        │
        ▼
AI-Powered Threat Analysis
        │
        ▼
SOC Triage Report
```

---

# 📂 Repository Structure

```text
AI-Based-Junior-SOC-Analyst/
│
├── README.md
│
├── resources/
│   ├── ai_soc_capture.py
│   ├── SOC_Playbook.txt
│   └── sample_alert.json
│
└── screenshots/
    ├── 01-Lab-Architecture.png
    ├── 02-Airia-AI-Agent.png
    ├── 03-Network-Traffic-Generation.png
    └── 04-Automated-Detection-and-AI-Response.png
```
---
### Repository Contents

| File / Folder | Description |
|---------------|-------------|
| **README.md** | Project documentation, setup guide, workflow, and usage instructions. |
| **resources/ai_soc_capture.py** | Python automation script responsible for packet capture, traffic analysis, JSON alert generation, and Airia AI integration. |
| **resources/SOC_Playbook.txt** | Custom SOC playbook used by Airia AI to perform automated alert validation, threat classification, risk scoring, MITRE ATT&CK mapping, and analyst recommendations. |
| **resources/sample_alert.json** | Example of the structured JSON alert generated by the Python automation before being sent to Airia AI. |
| **screenshots/** | Screenshots demonstrating the project architecture, AI agent configuration, network traffic generation, and automated detection workflow. |

This repository is organized to separate the implementation resources from the project documentation and visual assets, making it easier to understand, maintain, and extend.

---

---

# 🚀 Installation & Setup

Follow the steps below to set up and run the project in your own virtual lab environment.

## Prerequisites

Before running the project, ensure the following components are installed:

- Python 3.x
- TShark (Wireshark CLI)
- Oracle VirtualBox
- Ubuntu Linux Virtual Machine
- Kali Linux Virtual Machine
- Airia AI Account
- Published Airia AI Agent with API Endpoint and API Key

---

## Clone the Repository

```bash
git clone https://github.com/<your-github-username>/AI-Based-Junior-SOC-Analyst.git

cd AI-Based-Junior-SOC-Analyst
```

---

## Install Python Dependency

```bash
pip install requests
```

---

## Verify TShark Installation

```bash
tshark --version
```

If TShark is not installed:

### Ubuntu

```bash
sudo apt update
sudo apt install tshark
```

### Kali Linux

```bash
sudo apt update
sudo apt install tshark
```

---

## Configure Airia AI

Open the Python script located in the **resources** folder.

```text
resources/ai_soc_capture.py
```

Replace the following placeholders with your own Airia AI credentials.

```python
AIRIA_API_URL = "YOUR_AIRIA_PIPELINE_URL"
AIRIA_API_KEY = "YOUR_AIRIA_API_KEY"
```

Update the monitoring interface and destination IP according to your lab environment.

Example:

```python
INTERFACE = "eth0"
DESTINATION_IP = "192.168.56.101"
```

---

## Execute the Project

Navigate to the resources directory.

```bash
cd resources
```

Run the Python automation script.

```bash
python3 ai_soc_capture.py
```

The script will automatically perform the following operations:

1. Capture live network traffic using TShark.
2. Save the captured packets as a PCAP file.
3. Convert the PCAP file into CSV format.
4. Analyze packet activity.
5. Detect suspicious traffic based on the configured threshold.
6. Generate a structured JSON alert.
7. Send the alert to Airia AI.
8. Receive an AI-generated SOC triage report.

---

# ▶️ Usage

Once the environment is configured and the Python automation script is running, the project automatically monitors network traffic and performs AI-assisted security analysis.

## Step 1 — Generate Network Traffic

From the Ubuntu virtual machine, generate ICMP traffic towards the Kali Linux monitoring server.

```bash
ping 192.168.56.101
```

For testing higher traffic volumes, increase the number of packets.

```bash
ping -c 100 192.168.56.101
```

---

## Step 2 — Start the Monitoring Script

On the Kali Linux monitoring server, navigate to the project directory.

```bash
cd resources
```

Execute the automation script.

```bash
python3 ai_soc_capture.py
```

---

## Step 3 — Automated Detection Process

The Python script automatically performs the following tasks:

- Captures live ICMP traffic using TShark.
- Stores the captured packets as a PCAP file.
- Converts the PCAP file into CSV format.
- Counts packets received from each source IP address.
- Compares packet counts against the configured detection threshold.
- Generates a structured JSON security alert when suspicious activity is detected.
- Sends the generated alert to Airia AI using its REST API.
- Receives an AI-generated SOC triage report.

---

## Expected Output

A successful execution displays information similar to the following:

```text
[+] Capturing network traffic...
[+] Capture saved to traffic.pcap
[+] CSV created successfully.

Traffic volume per source IP:

192.168.56.106 : 30 packets

[!] Suspicious IP detected.

[+] Alert JSON generated.

[+] Sending alert to Airia AI...

[+] Airia responded with status 200

[+] SOC triage report received successfully.
```

After successful execution, the project produces:

- Captured PCAP file
- CSV traffic data
- Structured JSON alert
- AI-generated SOC triage report

These outputs demonstrate the complete end-to-end workflow from network traffic generation to automated AI-assisted security analysis.

---

# 📸 Project Screenshots

The following screenshots demonstrate the complete workflow of the project, from AI agent configuration to automated network traffic analysis and AI-assisted SOC triage.

---

## 1. Lab Architecture

The overall architecture of the project illustrates the end-to-end workflow, including traffic generation, packet capture, Python automation, JSON alert generation, Airia AI integration, and automated SOC analysis.

![Lab Architecture](screenshots/01-Lab-Architecture.png)

---

## 2. Airia AI Agent Configuration

A custom AI-based Junior SOC Analyst was created in Airia AI using a dedicated SOC playbook. The agent validates incoming alerts, classifies threats, calculates risk scores, maps activity to the MITRE ATT&CK Framework, and recommends analyst actions.

![Airia AI Agent](screenshots/02-Airia-AI-Agent.png)

---

## 3. Network Traffic Generation

Ubuntu Linux acts as the traffic generator within the virtual lab by sending ICMP packets to the Kali Linux monitoring server. This simulated traffic is used to validate the automated detection pipeline.

![Network Traffic Generation](screenshots/03-Network-Traffic-Generation.png)

---

## 4. Automated Detection & AI SOC Response

The Python automation running on Kali Linux captures live network traffic using TShark, analyzes packet activity, identifies suspicious network behavior based on a configurable threshold, generates a structured JSON alert, submits the alert to Airia AI, and receives an automated SOC triage report.

![Automated Detection and AI Response](screenshots/04-Automated-Detection-and-AI-Response.png)

---

# 📊 Project Outcomes

This project successfully demonstrates how Artificial Intelligence can assist a Security Operations Center (SOC) by automating the initial investigation and triage of network security alerts.

During testing, the complete detection pipeline was successfully executed, including network traffic generation, packet capture, traffic analysis, automated alert generation, and AI-assisted threat analysis.

### Successfully Implemented

- ✅ Live ICMP traffic generation in a virtual lab environment.
- ✅ Real-time packet capture using TShark.
- ✅ Automated packet analysis using Python.
- ✅ Threshold-based detection of suspicious network activity.
- ✅ Structured JSON alert generation.
- ✅ REST API integration with Airia AI.
- ✅ AI-powered SOC alert triage using a custom SOC playbook.
- ✅ Automated threat classification.
- ✅ Risk scoring and confidence assessment.
- ✅ MITRE ATT&CK framework mapping.
- ✅ Automated analyst recommendations.
- ✅ Executive summary generation for SOC analysts.

---

# 🎯 Skills Demonstrated

This project highlights practical cybersecurity and automation skills commonly required for Security Operations Center (SOC) roles.

### Cybersecurity

- Security Operations Center (SOC)
- Network Traffic Analysis
- Packet Capture & Analysis
- Threat Detection
- Incident Triage
- MITRE ATT&CK Framework

### Networking

- TCP/IP Fundamentals
- ICMP Traffic Analysis
- Network Monitoring
- Packet Inspection

### Programming

- Python Automation
- JSON Processing
- CSV Processing
- REST API Integration

### Tools & Platforms

- Kali Linux
- Ubuntu Linux
- TShark
- Wireshark
- Airia AI
- Oracle VirtualBox
- Git & GitHub

### Soft Skills

- Security Automation
- Analytical Thinking
- Problem Solving
- Technical Documentation

---

# 🚀 Future Improvements

The current implementation focuses on automated ICMP traffic analysis and AI-assisted SOC triage. Future enhancements can further improve the solution by expanding its detection capabilities and integrating additional security technologies.

- Real-time continuous packet monitoring.
- Support for TCP and UDP traffic analysis.
- Detection of port scanning and brute-force attacks.
- Zeek network monitoring integration.
- Suricata IDS integration.
- Wazuh SIEM integration.
- Threat Intelligence enrichment using VirusTotal.
- IP reputation lookup.
- Email and Slack alert notifications.
- Interactive SOC dashboard for visualization.
- Machine Learning-based anomaly detection.
- Multi-host monitoring support.

---

# ⚠️ Disclaimer

This project was developed exclusively for educational, research, and cybersecurity learning purposes.

The generated network traffic was created within an isolated virtual laboratory using authorized virtual machines. No unauthorized systems or production environments were targeted during the development or testing of this project.

The AI-generated security assessments should be treated as analyst assistance rather than a replacement for professional human investigation.

---

# 👨‍💻 Author

## Dhruv Kachchhi

Cybersecurity Enthusiast | SOC Analyst Aspirant

This project was developed to demonstrate practical SOC automation by integrating packet capture, Python-based traffic analysis, AI-assisted alert triage, and cybersecurity best practices into a single end-to-end workflow.

If you found this project helpful or interesting, consider giving this repository a ⭐ and connecting with me on LinkedIn.

---
