# SOC Detection Lab (Splunk + Sysmon + Active Directory)

Author: Jerald L. Burgess

## Overview

This project documents a hands-on Security Operations Center (SOC) detection lab designed to simulate enterprise security monitoring and incident investigation.

Technologies used:

• Splunk Enterprise SIEM
• Windows Event Logs
• Sysmon Endpoint Telemetry
• Active Directory Domain Environment
• Windows 10 Endpoint

This lab demonstrates practical SOC analyst skills including:

* Security monitoring
* Log analysis
* Incident investigation
* Detection engineering
* Threat hunting

---

# Lab Architecture

Environment components:

| System                     | Role                                             |
| -------------------------- | ------------------------------------------------ |
| Splunk Server              | Security Information and Event Management (SIEM) |
| DC01                       | Active Directory Domain Controller               |
| WIN10-CL1                  | Windows 10 endpoint workstation                  |
| Sysmon                     | Endpoint telemetry collector                     |
| Splunk Universal Forwarder | Log forwarding agent                             |

### Data Flow

Windows Endpoint
↓
Sysmon + Windows Logs
↓
Splunk Forwarder
↓
Splunk Enterprise SIEM
↓
Search & Investigation

---

# Data Sources

Logs ingested into Splunk include:

* WinEventLog:Security
* WinEventLog:System
* Microsoft-Windows-Sysmon/Operational

Key monitored events:

| Event ID | Description         |
| -------- | ------------------- |
| 4624     | Successful logon    |
| 4625     | Failed logon        |
| 4672     | Privileged logon    |
| Sysmon 1 | Process creation    |
| Sysmon 3 | Network connections |

---

# Incident Investigations

This repository documents SOC investigations including:

IR-001 – Privileged Logon Investigation (Event ID 4672)

Each investigation includes:

* Incident report
* Splunk queries
* Timeline reconstruction
* Evidence screenshots

---

# Skills Demonstrated

* SIEM deployment and log ingestion
* Windows log analysis
* Endpoint telemetry monitoring
* Privileged activity detection
* SOC investigation workflow
* Security documentation

---

# Future Enhancements

Planned improvements:

* Threat hunting queries
* Firewall telemetry integration
* OT device monitoring using Raspberry Pi
* Additional SOC investigation scenarios
