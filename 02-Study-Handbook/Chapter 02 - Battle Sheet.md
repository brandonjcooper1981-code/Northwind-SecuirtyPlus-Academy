# Chapter 2 Battle Sheet - Windows Fundamentals

## Windows Administrative Tools

| Tool | Purpose |
|------|---------|
|Event Viewer|Review logs|
|Computer Management|Administrative console|
|Device Manager|Hardware|
|Services|Background services|
|Task Manager|Processes|
|Disk Management|Storage|
|Local Users & Groups|Local accounts|

---

## Event IDs

| Event ID | Meaning |
|----------|----------|
|4624|Successful Logon|
|4625|Failed Logon|
|4634|Logoff|
|4688|Process Created|

- 4688 = One of the highest-yeild Event Ids on Security+.

---

## Windows Services

| Service | Purpose |
|----------|---------|
|DHCP Client|Receives IP|
|DNS Client|Name resolution|
|Windows Defender|Malware protection|
|Windows Update|Updates|
|Print Spooler|Printing|

---

## PowerShell Commands

| Command | Purpose |
|----------|---------|
|Get-Process|Running processes|
|Get-NetTCPConnection|Network connections|
|Get-NetIPAddress|IP configuration|
|Resolve-DnsName|DNS lookup|
|Get-DnsClientServerAddress|DNS servers|
|Get-NetRoute|Routing table|
|Get-CimInstance Win32_Service|Services|

---

## Windows Security

| Feature | Purpose |
|---------|---------|
|Windows Defender|Endpoint protection|
|Windows Firewall|Network protection|
|BitLocker|Disk encryption|
|UAC|Privilege control|

---

## Malware Investigation Workflow

User reports issue
↓
Event Viewer
↓
Security Logs
↓
4688
↓
PowerShell History
↓
Network Connections
↓
Windows Defender
↓
Containment

---

## Investigation Clues

| If You See... | Think... |
|----------------|----------|
|4625|Failed logon|
|4624 after failures|Possible compromise|
|4688|Process execution|
|Invoke-WebRequest|Investigate download|
|Trojan.Generic|Malware|
|Known malicious IP|Containment|

---

## Brandon's Memory Tricks

- 4688 = Process Created.
- PowerShell history tells the story.
- Failed Defender quarantine ≠ Safe system.
- Known malicious IP + malware = Isolate first.
- Containment comes before eradication.

