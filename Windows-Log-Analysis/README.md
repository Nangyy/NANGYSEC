# Windows Event Viewer & Log Analysis Lab

## Overview

Today I performed a practical Windows log analysis lab using Windows Event Viewer.

The goal was to understand how Windows records authentication activity and how a cybersecurity analyst can investigate these events.

## What I Practiced

- Navigating Windows Event Viewer
- Accessing Windows Security logs
- Filtering logs by Event ID
- Investigating successful and failed logons
- Analyzing Event ID 4624
- Analyzing Event ID 4625
- Understanding Logon Types
- Using XML View to examine event details
- Understanding Status and SubStatus
- Identifying the loopback address `127.0.0.1`

## Event ID 4625 — Failed Logon

I investigated a failed authentication event.

- Event ID: `4625`
- Logon Type: `2` — Interactive
- Target Username: `NANGY`
- Status: `0xc000006d`
- SubStatus: `0xc000006a`
- IP Address: `127.0.0.1`

The event showed that the authentication attempt failed because of an incorrect password.

The `127.0.0.1` address indicated that the activity originated from the local computer.

## Event ID 4624 — Successful Logon

I also investigated a successful logon event.

- Event ID: `4624`
- Target Username: `SYSTEM`
- Target Domain: `NT`
- Logon Type: `5` — Service
- IP Address: `-`

This helped me understand that not every successful logon represents a person manually logging into Windows. Logon Type 5 represents a service logon.

## XML View

I used:

**Details → XML View**

to examine structured event information such as:

- TargetUserName
- TargetDomainName
- Status
- SubStatus
- LogonType
- IpAddress
- LogonId

## Key Lesson

I learned that an Event ID alone does not automatically mean malicious activity.

A security analyst needs to examine:

**Event → Evidence → Context → Conclusion**

The surrounding information helps determine what actually happened.

## Evidence

Screenshots from my practical lab will be added to this project as evidence.

## Next Step

My next Windows log analysis exercise will be:

**Event ID 4688 — Process Creation**

I will investigate process creation events and learn how they can help during security investigations.

---

**Learning in public. One lab at a time. 🔐💻**

#CyberSecurity #Windows #LogAnalysis #EventViewer #SOC #BlueTeam
