# Investigating Network Activities on Linux Systems

## Introduction
![LINUX NETWORK FORENSICS](https://github.com/user-attachments/assets/4bdd32c9-5262-44da-8e15-85327ad2ff2b)

Network activity analysis is a fundamental skill in cybersecurity, helping you monitor, analyze, and troubleshoot network traffic and activities. This lab will guide you through basic network investigation techniques on a Linux system, allowing you to examine network interfaces, monitor traffic, and identify potential security issues.    

`Category`: Digital Forensics and Incident Response   
`Sub-Category`: Linux Forensics   
`Level`: Beginner   


## Pre-requisites

- Basic understanding of Linux commands and network concepts.
- A Linux system or virtual machine with sudo privileges.
- Familiarity with command-line interface (CLI).

## Lab Setup and Tools

### Lab Setup

1. Install a Linux distribution (e.g., Ubuntu, Fedora) on your system or set up a virtual machine using VirtualBox or VMware.
2. Ensure you have sudo access to install necessary tools and perform analysis.

### Tools

- `ifconfig` or `ip` - Display and configure network interfaces
- `netstat` - Network statistics
- `ss` - Socket statistics
- `tcpdump` - Network packet analyzer
- `nmap` - Network scanner
- `ping` - Network connectivity tester
- `traceroute` - Network path analyzer

## Exercises

### Exercise 1: Viewing and Configuring Network Interfaces
Objective: Understand how to view and configure network interfaces on a Linux system to ensure proper network connectivity and configuration.

Step 1. **View network interfaces using ifconfig:**
```bash
   ifconfig
```
Expected Output: List of all network interfaces with their IP addresses, MAC addresses, and other configuration details.

Step2: View network interfaces using ip:

```bash
ip addr show
```
Expected Output: Detailed information about all network interfaces, including IP addresses and state (up/down).

Step3: Bring an interface up:

```bash
sudo ifconfig eth0 up
```
Expected Output: No output if successful. The interface eth0 is now active.

Step4: Bring an interface down:

```bash
sudo ifconfig eth0 down
```
Expected Output: No output if successful. The interface eth0 is now inactive.

### Exercise 2: Analyzing Network Connections
Objective: Learn how to analyze active network connections to monitor network usage and detect potential anomalies.



Step1: Display active connections using netstat:

```bash
netstat -tunapl
```
Expected Output: List of all active TCP/UDP connections, including local and remote addresses, ports, and process IDs.

Step2: Display active connections using ss:

```bash
ss -tunapl
```
Expected Output: Similar to netstat, but with more detailed socket information.

Step3: List listening ports:

```bash
netstat -tuln
```
Expected Output: List of all listening ports and associated services.

### Exercise 3: Monitoring Network Traffic
Objective: Gain experience in capturing and analyzing network traffic to understand data flow and identify potential security threats.

Step1: Capture packets on a network interface:

```bash
sudo tcpdump -i eth0
```
Expected Output: Real-time display of packets being transmitted and received on eth0.

Step2: Save packet capture to a file:

```bash
sudo tcpdump -i eth0 -w capture.pcap
```
Expected Output: Packet data saved to capture.pcap file.

Step3: Read and analyze packet capture file:

```bash
tcpdump -r capture.pcap
```
Expected Output: Display of the contents of the capture.pcap file.

Exercise 4: Scanning and Mapping the Network
Objective: Learn how to scan and map network hosts and services to identify potential vulnerabilities and unauthorized devices.

Step1: Scan for live hosts on a network:

```bash
sudo nmap -sn 192.168.1.0/24
```
Expected Output: List of all live hosts on the specified subnet.

Step2: Perform a detailed scan on a host:

```bash
sudo nmap -A 192.168.1.1
```
Expected Output: Detailed information about the host, including operating system, open ports, and services.

Step3: Scan for open ports:

```bash
sudo nmap -p- 192.168.1.1
```
Expected Output: List of all open ports on the specified host.

### Exercise 5: Testing Network Connectivity and Path Analysis
Objective: Understand how to test network connectivity and analyze the path to remote hosts to troubleshoot network issues and ensure proper routing.

Step1: Test connectivity to a host:

```bash
ping google.com
```
Expected Output: Continuous ping results showing the round-trip time to google.com.

Step2: Analyze the path to a remote host:

```bash
traceroute google.com
```
Expected Output: List of all hops between your machine and google.com, including the IP address and response time of each hop.

Step3: Perform a reverse DNS lookup:

```bash
dig -x 8.8.8.8
```
Expected Output: Hostname associated with the IP address 8.8.8.8.

By completing these exercises, you will develop a foundational understanding of investigating network activities on Linux, an essential skill for network security and troubleshooting.




## About Me

I am a cybersecurity trainer with a passion for teaching and helping others learn essential cybersecurity skills through practical, hands-on projects. Connect with me on social media for more updates and resources:

[![LinkedIn](https://img.icons8.com/fluent/48/000000/linkedin.png)](https://www.linkedin.com/in/rajneeshcyber)
[![YouTube](https://img.icons8.com/fluent/48/000000/youtube-play.png)](https://www.youtube.com/@rajneeshcyber)
[![Twitter](https://img.icons8.com/fluent/48/000000/twitter.png)](https://twitter.com/rajneeshcyber)

Feel free to reach out with any questions or feedback. Happy learning!
