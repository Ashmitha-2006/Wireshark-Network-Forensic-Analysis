📌 Project Title

Network Traffic Analysis & Threat Investigation using Wireshark

🧠 Overview

This project presents a real-world network forensic investigation conducted using Wireshark to analyze a packet capture (PCAP) file and identify malicious activity within a network environment.

The investigation focuses on detecting suspicious behavior, reconstructing attacker actions, and performing device-level attribution using packet-level evidence.

🎯 Objective
Identify the source of malicious email activity
Analyze network traffic for suspicious patterns
Reconstruct attacker actions using packet data
Correlate evidence to support attribution


🛠️ Tools Used
Wireshark – Packet inspection and analysis
TCP Stream Reconstruction – Extracting application-layer data
Protocol Filtering – HTTP, DNS, TCP analysis


🔍 Investigation Approach
The investigation followed a structured forensic methodology:

Traffic Analysis
Identified high-activity hosts using endpoint statistics
Filtering & Isolation
Applied filters such as:
ip.addr == 192.168.15.4
http, dns
http.request.method == "POST"
Protocol Analysis
Examined HTTP and DNS communications
TCP Stream Reconstruction
Recovered email content from unencrypted traffic
Correlation & Attribution
Linked network activity with authenticated user sessions



🚨 Key Findings
🔴 Primary Suspect Identified
IP: 192.168.15.4 generated the highest network activity
🌐 Suspicious External Communication
Traffic to anonymous messaging service detected
📤 Malicious HTTP POST Request
Email sent via /secure/submit endpoint
🔓 Unencrypted Data Exposure
Email content transmitted in plaintext
👤 Authenticated Session Detected
Gmail session linked to suspect device
🎯 Strong Attribution Evidence
Same device performed browsing + message submission


⏱️ Attack Timeline
Google session initiated
Gmail authentication detected
Navigation to anonymous messaging service
HTTP POST request submitted
Server returns success response (302)
Session terminated


💥 Impact
Exposure of sensitive data due to lack of encryption
Misuse of anonymous communication platforms
Demonstrates how attacker actions can be reconstructed from network traffic


🧠 Skills Demonstrated
Network Traffic Analysis
Packet Inspection & Filtering
TCP Stream Reconstruction
Threat Investigation
Digital Forensics
Evidence Correlation
