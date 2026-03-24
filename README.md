# Windows Brute Force Detection Lab

## Objective
Simulate a brute force attack on a Windows system and detect it using Splunk.  
The goal is to identify failed and successful login patterns indicative of a brute-force attack.

## Tools Used
- **Attack:** Hydra (Kali Linux)
- **Target:** Windows VM
- **Detection:** Splunk (Security Event Logs)

## Attack Simulation
- Target account: Administrator
- Method: SMB login brute force
- Commands used on Kali:
```bash
hydra -l Administrator -P passwords.txt smb://<target-ip> -V
