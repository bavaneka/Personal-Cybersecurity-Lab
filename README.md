# Personal-Cybersecurity-Lab-Build

## 📖 Overview
This repository contains the documentation and evidence for Task 2 of my cybersecurity internship at Maincraft Technologies. The objective of this task was to design and build a safe, isolated penetration testing environment from scratch on a local machine.
Having an isolated lab is critical for offensive security, as it allows for the safe execution of exploits and analysis of malware without risking exposure to real-world home networks or the internet.

## 🏗️ Architecture
The lab was built using virtualization and containerization to ensure strict network segmentation.
- **Host OS:** Windows
- **Virtualization Platform:** Oracle VirtualBox
- **Attacker Machine:** Kali Linux (Allocated 2 CPUs, 2GB RAM)
- **Target Application:** OWASP Juice Shop (Intentionally vulnerable web app)

### 🌐 Network Segmentation
A dual-adapter network configuration was utilized for the Kali Linux VM:
1. **NAT Adapter:** Provided outbound internet access strictly for downloading packages and updates.
2. **Host-Only Adapter:** Created a closed-loop, isolated network (`192.168.56.0/24`) where all attack traffic is safely contained.
## 🛠️ Tools Mastered

During the deployment and validation of this lab, the following core cybersecurity tools were utilized:
* **Docker:** Used to rapidly deploy the vulnerable target application on the isolated network.
* **Nmap:** Executed subnet scanning to perform host discovery and validate network connectivity.
* **Burp Suite:** Configured proxy settings to successfully intercept, pause, and analyze live HTTP `GET` requests between the browser and the target server.
* **Wireshark:** Attached to the Host-Only interface (`eth1`) to perform live packet capture and analyze raw ICMP network traffic.

## 📁 Evidence
* The full step-by-step documentation and visual screenshot evidence of the lab build, network configuration, and tool validation have been compiled into a final PDF report.

## 🚀 Learnings
This project reinforced that offensive security relies heavily on a deep understanding of network architecture. By manually configuring the virtual adapters and verifying packet flow, I gained a much stronger grasp of how traffic moves across segmented networks. This lab will now serve as my primary sandbox for future web application hacking and incident response practice.
