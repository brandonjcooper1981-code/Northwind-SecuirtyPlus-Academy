# Chapter 1 Battle Sheet - Networking Fundamentals

## Networking Essentials

| If you See... | Think... |
|----------------|----------|
| 169.254.x.x | APIPA → DHCP problem |
| Can ping IP but not hostname | DNS problem |
| No IP address | DHCP |
| No gateway response | Local network problem |
| Gateway works, Internet doesn't | Router/ISP issue |

---

## TCP/IP

| Protocol | Remember |
|----------|----------|
| TCP | Reliable, connection-oriented |
| UDP | Fast, connectionless |
| IP | Addressing & routing |
| ICMP | Diagnostics (ping) |

---

## IPv4

Know these four immediately:
- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

---

## DHCP

Remember:
- DORA:
    - Discover
    - Offer
    - Request
    - Acknowledge

If you see 169.254.x.x...
- Think DHCP first, not DNS

---

## DNS

DNS converts:
www.google.com
↓
142.x.x.x

Security+ Favorite:
- Works by IP, fails by hostname = DNS

---

## Common Ports

| Port | Service |
|------|----------|
|20/21|FTP|
|22|SSH|
|23|Telnet|
|25|SMTP|
|53|DNS|
|67/68|DHCP|
|80|HTTP|
|110|POP3|
|143|IMAP|
|389|LDAP|
|443|HTTPS|
|445|SMB|
|3389|RDP|

---

## Troubleshooting Order

Cable/Wi-Fi
↓
IP Address
↓
DHCP
↓
DNS
↓
Gateway
↓
Internet
↓
Application

---

## Exam Triggers

| If You See... | Think... |
|----------------|----------|
|169.254.x.x|DHCP|
|Can ping IP only|DNS|
|Port 53|DNS|
|Port 445|SMB|
|Port 3389|RDP|
|HTTPS|443|

---

## Brandon's Memory Tricks

- 169.254 = DHCP until proven otherwise.
- Hostname fails = DNS.
- TCP = Reliable.
- UDP = Fast.
- DNS = 53.
- HTTPS = 443.
- SMB = 445.