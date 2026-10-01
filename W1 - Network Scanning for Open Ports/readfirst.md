# Task 1: Scan Your Local Network for Open Ports

## Objective
Learn to discover open ports on devices in a local network and understand potential security risks associated with exposed services.

## Tools Used
- Nmap
- Wireshark (Optional)

## Scan Performed

```bash
nmap -sn 192.168.191.128/24
nmap -T4 -F 192.168.191.128/24
```

## Open Ports Discovered

| Port | Service |
|--------|---------|
| 53/tcp | DNS |
| 80/tcp | HTTP |
| 7070/tcp | Web Application / Proxy / Custom Service |
| 3306/tcp | MySQL / MariaDB |

## Common Services Running on These Ports

### 53/tcp
- Domain Name System (DNS)
- Used for translating domain names into IP addresses.

### 80/tcp
- HyperText Transfer Protocol (HTTP)
- Hosts websites and web applications.

### 7070/tcp
- Often used by web applications, proxy services, or custom application servers.

### 3306/tcp
- MySQL/MariaDB Database Service
- Used to store and manage application data.

## Potential Security Risks

### 53/tcp
- DNS misconfigurations may allow zone transfers or DNS amplification attacks.

### 80/tcp
- Traffic is unencrypted and may expose sensitive information.
- Vulnerable web applications can be exploited.

### 7070/tcp
- Administrative panels or custom services may be exposed.
- Weak authentication could allow unauthorized access.

### 3306/tcp
- Database exposure may lead to data theft.
- Vulnerable to brute-force attacks if not properly secured.

---

# Interview Questions & Answers

### 1. What is an open port?
An open port is a network port that is actively accepting incoming connections or requests.

### 2. How does Nmap perform a TCP SYN scan?
Nmap sends a SYN packet and analyzes the response without completing the full TCP handshake.

### 3. What risks are associated with open ports?
Open ports can expose services that attackers may exploit to gain unauthorized access.

### 4. Explain the difference between TCP and UDP scanning.
TCP scanning checks connection-oriented services, while UDP scanning checks connectionless services.

### 5. How can open ports be secured?
Close unused ports, apply firewall rules, update services, and enforce strong authentication.

### 6. What is a firewall's role regarding ports?
A firewall controls which ports and services are allowed to send or receive network traffic.

### 7. What is a port scan and why do attackers perform it?
A port scan identifies open ports and services to find potential attack surfaces.

### 8. How does Wireshark complement port scanning?
Wireshark captures and analyzes network traffic, helping verify and investigate scan results.

## Outcome
- Learned basic network reconnaissance.
- Identified exposed services on the local network.
- Understood security risks associated with open ports.
- Gained practical experience using Nmap.

## Key Concepts
- Port Scanning
- TCP SYN Scan
- IP Ranges
- Network Reconnaissance
- Open Ports
- Network Security Basics
