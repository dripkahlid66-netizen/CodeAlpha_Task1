# CodeAlpha Task 1: Basic Network Sniffer

## Project Overview
A Python-based network packet sniffer that captures and analyzes live network traffic packets in real-time.

## What It Does
✅ Captures network packets using Scapy library
✅ Analyzes packet structure and content
✅ Displays source and destination IP addresses
✅ Shows protocol information (ICMP for ping)
✅ Demonstrates data flow through network

## Requirements
- Python 3.x
- Scapy library
- Linux/Kali Linux
- Root/sudo access

## Installation
```bash
pip3 install scapy
```

## Usage
```bash
sudo python3 packet_sniffer_filtered.py
```

## How It Works
The sniffer captures ICMP packets (ping traffic) and displays:
- Packet number
- Timestamp
- Source IP
- Destination IP
- Protocol type

FILE used: packet_sniffer_filtered.py
<img width="1250" height="1366" alt="Screenshot 2026-10-10 132350" src="https://github.com/user-attachments/assets/1b91c1cc-de6a-4d8d-a9a8-250b536370ff" />

## Sample Output
[PACKET #1] 13:11:42
Source IP: 10.0.2.5
Destination IP: 8.8.8.8
Type: ICMP (Ping)

[PACKET #2] 13:11:42
Source IP: 8.8.8.8
Destination IP: 10.0.2.5
Type: ICMP (Ping)

# Screenshots - Task 1
<img width="1250" height="1366" alt="Screenshot 2026-10-10 131636" src="https://github.com/user-attachments/assets/acd2f4b1-6a18-4e23-a866-cc0749388294" />
<img width="1250" height="1366" alt="Screenshot 2026-10-10 131624" src="https://github.com/user-attachments/assets/f21e5f22-cee1-43a3-a067-c688cc9adf9a" />

## Packet Sniffer in Action
- Terminal showing packet capture
- Output displaying ICMP packets
- Source/destination IPs and protocols

## What I Learned
✅ How to capture network packets
✅ Understanding packet layers and structure
✅ Network protocols (IP, ICMP)
✅ Real-time traffic analysis
✅ Using Python Scapy library

## Task Completion
- ✅ Built Python program to capture packets
- ✅ Analyzed packet structure and content
- ✅ Learned data flow through networks
- ✅ Used Scapy library for packet capturing
- ✅ Displayed source/destination IPs and protocols

---
**CodeAlpha Cybersecurity Internship - Task 1**

Author: Dominic Joshua
