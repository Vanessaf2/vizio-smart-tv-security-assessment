# Vizio Smart TV Security Assessment

![Status](https://img.shields.io/badge/Status-Completed-success)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-blue)
![Tools](https://img.shields.io/badge/Tools-Wireshark%20%7C%20Nmap%20%7C%20pyvizio-orange)

## Project Overview

This project examined the security of a Vizio Smart TV by analyzing its SmartCast API, authentication process, exposed network services, and encrypted communications. The assessment was conducted from a Kali Linux virtual machine and focused on how IoT devices communicate across a local network, how authentication mechanisms protect device functionality, and what security risks may exist when services are exposed to other systems on the same subnet.

## Objectives

* Identify the Smart TV on the local network
* Discover exposed services and open ports
* Analyze SmartCast API authentication
* Execute authenticated API commands
* Capture and analyze network traffic
* Evaluate security implications of exposed IoT services

## Technologies Used

* Kali Linux
* Nmap
* Wireshark
* curl
* pyvizio
* VMware Workstation

## Lab Environment
* Attacker System: Kali Linux Virtual Machine
* Target Device: Vizio Smart TV with SmartCast enabled
* Hypervisor: VMware Workstation
* Communication Method: SmartCast API over HTTPS/TLS
* Network Type: Local Area Network (LAN)

## Investigation Methodology

### Device Discovery

The Smart TV was identified through network reconnaissance using Nmap host discovery scans. Device information, IP addressing, and vendor identification were collected to confirm network visibility.

### Service Enumeration

Targeted scans were performed to identify exposed services. The SmartCast API service was discovered on TCP port 7345 and analyzed as the primary communication interface.

### Authentication Analysis

The SmartCast pairing process was examined to understand how the device generates challenge tokens, requires PIN-based authentication, and issues authorization tokens for future API requests.

### API Command Execution

Authenticated API requests were executed using curl and pyvizio to validate SmartCast functionality, including volume control and device interaction.

### Network Traffic Analysis

Wireshark was used to capture traffic generated during API communication. TCP connection establishment, TLS 1.2 negotiation, encrypted application traffic, retransmissions, and session termination behavior were analyzed.

## Analysis Findings

* SmartCast API service was exposed on TCP port 7345
* Device authentication relied on PIN-based pairing and token generation
* Communications were protected using TLS 1.2 encryption
* Encrypted traffic still revealed timing, flow, and communication patterns
* Authenticated commands successfully controlled device functionality
* Exposed IoT services increase the visible attack surface of a local network

## Skills Demonstrated

* Network Traffic Analysis
* Packet Capture Investigation
* Service Enumeration
* API Security Analysis
* TLS Communication Analysis
* Network Reconnaissance
* Security Documentation
* Technical Troubleshooting
* Encrypted Traffic Analysis

## Screenshots

### Network Discovery

<img width="725" height="402" alt="image" src="https://github.com/user-attachments/assets/6d1d7b43-486b-4975-821e-4a1a9411a262" />


### SmartCast Service Enumeration

(Add screenshot)

### Authentication Token Generation

(Add screenshot)

### API Command Execution

(Add screenshot)

### TLS Handshake Analysis

(Add screenshot)

### Encrypted Application Traffic

(Add screenshot)

## Conclusion

This project provided hands-on experience investigating network communications, analyzing encrypted traffic, identifying exposed services, and documenting security observations. Through the use of Nmap, Wireshark, SmartCast API analysis, and network reconnaissance techniques, I developed practical skills in traffic analysis, security investigation, and technical troubleshooting that are applicable to security operations and network defense environments.
