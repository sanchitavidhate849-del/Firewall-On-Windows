# Firewall Configuration and Traffic Filtering

## Overview
This project demonstrates how to configure and manage firewall rules on both Windows and Linux systems.  
It includes listing current rules, blocking specific ports, allowing required services, and restoring original configurations.

## Tools Used
- **Windows Firewall** (GUI & PowerShell)
- **UFW** (Uncomplicated Firewall) for Linux

## Steps Followed

1. **Open Firewall Configuration Tool**  
   - Windows: Control Panel → Windows Defender Firewall → Advanced Settings  
   - Linux: Terminal with `ufw` commands

2. **List Current Firewall Rules**  
   - Windows: `netsh advfirewall firewall show rule name=all` (or via GUI)  
   - Linux: `sudo ufw status numbered`

3. **Block Inbound Traffic on Port 23 (Telnet)**  
   - Windows: `netsh advfirewall firewall add rule name="Block Telnet" dir=in action=block protocol=TCP localport=23`  
   - Linux: `sudo ufw deny 23`

4. **Test the Rule**  
   - Attempt Telnet connection locally or from another system: `telnet <IP> 23`

5. **Allow SSH (Port 22) – Linux**  
   - `sudo ufw allow 22`

6. **Remove Test Block Rule**  
   - Windows: `netsh advfirewall firewall delete rule name="Block Telnet"`  
   - Linux: `sudo ufw delete deny 23`

7. **Document Steps**  
   - Commands and GUI procedures saved for reference.

8. **Traffic Filtering Summary**  
   Firewalls control network traffic based on pre-configured rules. They inspect packets and allow or block them based on IP addresses, ports, and protocols, protecting the system from unauthorized access.

## Output Files
- `report.txt`: Command outputs and test results
- `references.txt`: Related resources
# Firewall-On-Windows
