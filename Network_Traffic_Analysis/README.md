# Network Traffic Analysis using Wireshark, tcpdump, and Snort

## Introduction

This project demonstrates practical network traffic capture and analysis performed on Kali Linux using industry-standard cybersecurity tools. The main objective of this project is to understand how network packets flow, how ICMP traffic works, and how security tools analyze and detect suspicious or abnormal network behavior.

The project uses Wireshark for graphical packet analysis, tcpdump for command-line packet capture, and Snort as a basic intrusion detection system (IDS). All activities were performed on a local system strictly for educational and learning purposes.

---

## Objectives of the Project

- To capture live network traffic using Wireshark
- To analyze ICMP packets generated using ping
- To understand packet structure and protocol fields
- To capture traffic using tcpdump from the command line
- To observe basic traffic analysis and alerts using Snort
- To gain hands-on experience with network security tools

---

## Tools and Technologies Used

- Operating System: Kali Linux
- Network Interface: eth0
- Packet Analyzer (GUI): Wireshark
- Packet Capture Tool (CLI): tcpdump
- Intrusion Detection System: Snort
- Network Utility: ping

---

## Network Traffic Analysis using Wireshark

### Step 1: Launch Wireshark

Wireshark was started from the terminal using the following command:

wireshark

After launching, the network interface **eth0** was selected for live packet capture.

---

### Step 2: Generate ICMP Traffic

To generate network traffic, ICMP echo requests were sent using the ping command:

ping google.com

This command generates ICMP packets which are captured live in Wireshark.

---

### Step 3: ICMP Packet Analysis

Captured ICMP packets were filtered using the following display filter:

icmp

The packet list and detailed packet structure were analyzed, including:
- Source and destination IP addresses
- ICMP type and code
- Time-to-live (TTL)
- Packet length and payload data

---

## Network Traffic Capture using tcpdump

### Step 4: Start Packet Capture with tcpdump

tcpdump was used to capture packets directly from the terminal:

sudo tcpdump -i eth0

This command captures all traffic passing through the eth0 interface.

---

### Step 5: Limited Packet Capture

To capture a limited number of packets for analysis:

sudo tcpdump -i eth0 -c 20

This command captures 20 packets and stops automatically.

---

### Step 6: Observations from tcpdump

The tcpdump output showed:
- ICMP echo requests and replies
- ARP requests and replies
- Source and destination IP addresses
- Protocol information and packet length

---

## Traffic Analysis using Snort

### Step 7: Run Snort in Alert Mode

Snort was executed in alert mode to observe traffic behavior:

sudo snort -i eth0 -A alert_fast

Snort monitored live traffic and displayed packet statistics after stopping the capture.

---

### Step 8: Snort Analysis Results

Snort provided:
- Total packets analyzed
- Protocol-wise packet statistics
- Detection module summary
- TCP checksum warnings and traffic details

This demonstrates how an IDS observes and analyzes live network traffic.

---

## Results and Observations

- ICMP traffic generated using ping was successfully captured
- Wireshark provided detailed packet-level visibility
- tcpdump confirmed packet flow at the command-line level
- Snort analyzed traffic and displayed detection statistics
- Network behavior and packet structure were clearly understood

---

## Conclusion

This project successfully demonstrates basic network traffic analysis using Wireshark, tcpdump, and Snort. It provides hands-on understanding of packet capture, ICMP traffic analysis, and intrusion detection concepts. These tools are essential for cybersecurity professionals to monitor, analyze, and secure networks.

---

## Disclaimer

This project is created strictly for educational purposes. All activities were performed on a local system owned by the user. Unauthorized monitoring or testing of networks without proper permission is illegal and unethical.
