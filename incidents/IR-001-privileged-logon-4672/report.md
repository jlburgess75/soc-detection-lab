# IR-001 – Privileged Logon Investigation

## Alert

Splunk detected Windows Security Event ID **4672**, indicating that special privileges were assigned to a new logon session.

## Host

WIN10-CL1.corp.local

## User

CORP\labuser

## Event Source

WinEventLog:Security

## Event Details

Event ID: 4672
Description: Special privileges assigned to new logon.

This event occurs when an account logs into a system and receives administrative-level privileges.

## Investigation Steps

1. Search Splunk for privileged logon events.
2. Identify the associated successful login event.
3. Review process execution activity using Sysmon logs.
4. Review network connections originating from the host.

## Findings

A privileged logon event occurred for user **labuser** on workstation **WIN10-CL1**.

Further investigation should confirm whether this activity was legitimate administrative usage.

## Recommendation

Monitor privileged logon activity and generate alerts when privileged sessions occur on non-administrative systems.

## Evidence

Splunk queries and screenshots are stored in this investigation folder.
