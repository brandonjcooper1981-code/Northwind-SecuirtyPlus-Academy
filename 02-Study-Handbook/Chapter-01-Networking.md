# Chapter 01 – Networking Fundamentals

---

## Overview

Networking is one of the most important topics on the CompTIA Security+ exam. Nearly every security technology—from Active Directory to cloud computing, malware analysis, and incident response—depends on a solid understanding of how devices communicate across a network.

This chapter introduces the networking concepts that form the foundation of cybersecurity, including TCP/IP, IP addressing, DNS, DHCP, common protocols, ports, and troubleshooting methodologies.

Understanding these concepts will improve both Security+ exam performance and real-world troubleshooting skills.

---

## Learning Objectives

After completing this chapter you should be able to:

- Explain the purpose of TCP/IP
- Understand IPv4 addressing
- Explain DHCP and the DORA process
- Identify APIPA addresses
- Explain DNS resolution
- Identify common network protocols
- Memorize Security+ ports
- Apply a structured troubleshooting methodology

---

## Table of Contents

1. Networking Fundamentals
2. TCP/IP
3. IPv4 Addressing
4. DHCP
5. APIPA
6. DNS
7. Common Ports
8. Network Troubleshooting
9. Security+ Exam Tips
10. Brandon's Takeaways
11. Chapter Summary
12. Security+ Exam Watchlist
13. Quick Quiz

---

## What is a Network?

A network is a collection of devices that communicate with one another to share information and resources.

Examples include:
- Computers
- Servers
- Smartphones
- Printers
- Firewalls
- Switches
- Routers

Networks allow users to:
- Share files
- Access the Internet
- Authenticate to Active Directory
- Access cloud resources
- Communicate securely

---

## Types of Networks

| Type | Description |
|-------|-------------|
| LAN | Local Area Network |
| WAN | Wide Area Network |
| WLAN | Wireless Local Area Network |
| MAN | Metropolitan Area Network |
| PAN | Personal Area Network |

---

## TCP/IP

TCP/IP is the communication standard used by nearly every modern network.

It defines how devices:

- Address each other
- Send information
- Receive information
- Route information

| Protocol | Purpose |
|-----------|---------|
| TCP | Reliable communication |
| UDP | Fast communication |
| IP | Addressing and routing |
| ICMP | Network diagnostics |

### Why This Matters

Understanding TCP/IP is essential because nearly every Security+ PBQ involving networking, malware, cloud, or Active Directory relies on these protocols.

---

## IPv4

Explain:
- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

Example:
IP Address:      192.168.56.100

Subnet Mask:     255.255.255.0

Gateway:         192.168.56.1

DNS Server:      192.168.56.10

---

## DHCP

Dynamic Host Configuration Protocol automatically assigns:

- IP Address
- Subnet Mask
- Gateway
- DNS Server

DORA Table

| Step | Meaning |
|-------|----------|
| D | Discover |
| O | Offer |
| R | Request |
| A | Acknowledge |

---

## APIPA
### Security+ Exam Tip

169.254.x.x
↓
Think DHCP FIRST. NOT DNS.

### DNS

DNS Converts:
Northwind Example:

CLIENT01 joins
lab.local
↓
DNS resolves
DC01
↓
Domain Join succeeds

Common Symptoms
| Symptom | Likely Problem |
|----------|----------------|
| Can browse by IP | DNS |
| Can ping gateway only | Connectivity |
| 169.254.x.x | DHCP |

⚠ Security+ Exam Alert

If you can ping an IP address
but NOT a hostname
↓
Think DNS

Scenario:

A user reports:
"I can ping 8.8.8.8 but I can't browse to Google."

Question: 
Where do you begin troubleshooting?

Answer: 
DNS

---

## Common Ports

| Port | Protocol | Purpose |
|------|----------|----------|
| 20/21 | FTP | File Transfer |
| 22 | SSH | Secure Remote Login |
| 23 | Telnet | Insecure Remote Login |
| 25 | SMTP | Send Email |
| 53 | DNS | Name Resolution |
| 67/68 | DHCP | Address Assignment |
| 80 | HTTP | Web |
| 110 | POP3 | Download Email |
| 143 | IMAP | Sync Email |
| 389 | LDAP | Directory Services |
| 443 | HTTPS | Secure Web |
| 445 | SMB | Windows File Sharing |
| 3389 | RDP | Remote Desktop |

---

## Troubleshooting Flow

Can't Connect
↓
Check Physical Connection
↓
Check IP Address
↓
169.254?
↓
DHCP
↓
Default Gateway
↓
DNS
↓
Ping Gateway
↓
Ping Internet
↓
Resolve Hostname
↓
Firewall
↓
Application

---

## Brandon's Takeaways

✔ 169.254.x.x → Think DHCP before DNS.

✔ If it works by IP but not hostname → Check DNS.

✔ TCP = Reliable.

✔ UDP = Faster but no guarantee.

✔ DNS = Port 53.

✔ DHCP = Ports 67/68.

✔ SMB = Port 445.

✔ HTTPS = Port 443.

✔ Event ID 4688 = Process Created.

✔ Known malicious IP + failed Defender quarantine = Containment.

---

## Chapter Summary

In this chapter you learned:

- Networking fundamentals
- TCP/IP
- IPv4 addressing
- DHCP
- APIPA
- DNS
- Common Security+ ports
- Network troubleshooting methodology

These concepts form the foundation for many Security+ exam objectives and are essential for real-world Help Desk, Systems Administration, and Security Operations roles.

---

## Security+ Exam Watchlist

| If You See... | Think... |
|---------------|----------|
| `169.254.x.x` | DHCP |
| Can browse by IP but not hostname | DNS |
| Port 22 | SSH |
| Port 53 | DNS |
| Port 445 | SMB |
| Port 3389 | RDP |
| `ping 8.8.8.8` works, hostname fails | DNS resolution |
| APIPA | DHCP failure |

---

## Quick Quiz

1. Which port does DNS use?

2. What does APIPA indicate?

3. Which protocol is reliable?

4. Which protocol is connectionless?

5. Which protocol assigns IP addresses?

---

**Northwind Security+ Academy**

**Chapter:** 01 – Networking Fundamentals

**Version:** 1.0

**Status:** Complete

**Last Updated:** July 2026

**Next Chapter:** Windows Fundamentals

---