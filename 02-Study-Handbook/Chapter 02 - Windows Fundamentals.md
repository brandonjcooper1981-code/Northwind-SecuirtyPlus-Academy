# Chapter 02 – Windows Fundamentals

---

## Overview

Microsoft Windows is the most widely deployed operating system in enterprise environments and serves as the foundation for many Security+ objectives. Security analysts, help desk technicians, and system administrators rely on Windows tools to troubleshoot systems, investigate incidents, manage users, and secure endpoints.

This chapter introduces the Windows components most relevant to the CompTIA Security+ exam and provides practical examples based on the Northwind Technologies home lab.

---

## Learning Objectives

After completing this chapter you should be able to:

- Navigate core Windows administrative tools
- Understand Windows Event Logs
- Identify common Windows Event IDs
- Understand Windows services
- Use common PowerShell commands
- Understand Windows security features
- Apply a structured troubleshooting methodology

---

## Table of Contents

1. Key Terms
2. Windows Architecture
3. Administrative Tools
4. Event Viewer
5. Windows Event IDs
6. Windows Services
7. PowerShell
8. Try It Yourself
9. Windows Security Features
10. Troubleshooting Workflow
11. Security+ Exam Tips
12. Brandon's Takeaways
13. Chapter Summary

---

## Key Terms

- Kernel
- Registry
- NTFS
- PowerShell
- Event Viewer
- 4624
- 4625
- 4688
- Windows Defender
- BitLocker
- UAC

---

## Windows Architecture

| Component | Purpose |
|-----------|---------|
| Kernel | Core of the operating system |
| User Mode | Runs applications |
| Registry | Configuration database |
| Services | Background processes |
| Drivers | Hardware communication |
| File System (NTFS) | File storage and permissions |

---

## Administrative Tools

| Tool | Purpose |
|------|---------|
| Event Viewer | Review system and security logs |
| Computer Management | Central administration console |
| Device Manager | Hardware troubleshooting |
| Task Manager | Running processes and performance |
| Services | Manage background services |
| Disk Management | Storage management |
| Local Users and Groups | Manage local accounts |

💡 Northwind Example
    During the Active Directory Home Lab, Event Viewer and Computer Management were used to troubleshoot domain joins and service issues.

---

## Event Viewer

| Log | Purpose |
|-----|---------|
| Security | Authentication and auditing |
| System | Drivers, hardware, operating system |
| Application | Application events |
| Setup | Installation events |
| Forwarded Events | Remote log collection |

---

## Common Event IDs

| Event ID | Meaning |
|----------|---------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4634 | Logoff |
| 4688 | Process Created |

Norhtwind Example:
4625
4625
4624
4688 powershell.exe

This sequence often indicates:
- Failed login attempts
- Successful authentication
- Process execution

---

## Windows Services

| Service | Purpose |
|----------|---------|
| DHCP Client | Receives IP addresses |
| DNS Client | Resolves names |
| Windows Defender | Endpoint protection |
| Windows Update | Updates Windows |
| Print Spooler | Printing services |

---

## PowerShell

| Command | Purpose |
|----------|---------|
| `Get-Process` | Running processes |
| `Get-NetTCPConnection` | Active network connections |
| `Get-NetIPAddress` | IP configuration |
| `Resolve-DnsName` | DNS lookup |
| `Get-DnsClientServerAddress` | DNS servers |
| `Get-NetRoute` | Routing table |
| `Get-CimInstance Win32_Service` | Windows services |

💡 Northwind Example
    Get-Process -Id 4488

---

## Try It Yourself

- Get-Process
- Get-NetIPAddress
- Resolve-DnsName google.com
- Get-NetTCPConnection

What information did each commend provide?

---

## Windows Security Features

| Feature | Purpose |
|----------|---------|
| Windows Defender | Malware protection |
| Windows Firewall | Network filtering |
| BitLocker | Disk encryption |
| UAC | User Account Control |
| Microsoft Defender Firewall | Network security |

---

## Troubleshooting Workflow

User Reports Problem
↓
Event Viewer
↓
Security Log
↓
Process Creation
↓
PowerShell History
↓
Network Connections
↓
Services
↓
Incident Response

---

## Security+ Exam Tips

4688
↓
Process Created

4625
↓
Failed Login

4624
↓
Successful Login

Windows Defender
↓
Failed Quarantine
↓
Assume Compromise

> [!IMPORTANT]
> **Security+ Exam Alert**
>
> Event ID **4688** = Process Creation
>
> If CompTIA asks which log provides evidence that a process executed...
>
> Think **4688**.

---

## Brandon's Takeaways

✔ Event ID 4688 is one of the strongest indicators that a process executed.

✔ Security logs are usually the first place to investigate authentication events.

✔ Defender failing to quarantine does NOT mean the threat is gone.

✔ PowerShell history can reveal malicious downloads.

✔ Event Viewer + PowerShell + Network Connections often tell the complete story.

---

## Chapter Summary

This chapter introduced the Windows tools and security concepts most frequently encountered on the CompTIA Security+ exam and in enterprise environments.

Topics covered included:

- Windows architecture
- Administrative tools
- Event Viewer
- Event IDs
- Windows services
- PowerShell
- Windows security features
- Troubleshooting methodology

Mastering these concepts provides the foundation for incident response, malware analysis, and Windows administration.

---

## Analyst Checklist

Imagine you receive a suspicious workstation. Before taking action, ask:
Are there failed logon attempts (4625)?
Was there a successful logon (4624)?
Did any suspicious processes start (4688)?
Is PowerShell history available?
Are there active outbound connections?
Did Defender detect malware?
Was the malware successfully quarantined?
Is the destination IP known to be malicious?
Does the timeline support a compromise?