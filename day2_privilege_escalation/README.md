# Day 2 – Privilege Escalation Detection Lab

## Objective
Detect admin privilege escalation events in Windows logs for a compromised user.

## Overview
Continuing from Day 1, where the user `hacker` was compromised via brute force:

> After gaining access, the `hacker` account was escalated to administrative privileges and detected using Splunk.

This demonstrates **how SOC analysts detect suspicious privilege escalation post-compromise**.

## Attack Simulation
- **User involved:** hacker (normal user from Day 1)  
- **Privilege escalation command:**
```bat
net localgroup administrators hacker /add
