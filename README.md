# Stop the Smart Home Breach

## Overview
This project analyzes a real-world IoT to corporate attack scenario involving a compromised smart thermostat. The goal is to identify how the attack could be prevented and how each stage could be detected.

## Scenario Summary
A CEO’s smart thermostat was left with default settings and connected to a home network. An attacker gained access to the device, moved laterally across the network, captured VPN credentials, and accessed corporate financial systems.

## Attack Breakdown and Security Controls

### 1. Internet Scanning for IoT Devices
Vulnerability:
Exposed IoT devices with weak network configuration

Prevention:
- Network segmentation using VLANs for IoT devices
- Disable unnecessary ports and services
- Regular firmware updates
- Apply access control lists (ACLs)
- Use NAC to enforce device compliance

Detection:
- Monitor firewall and router logs for scanning activity
- Use IDS/IPS with threat intelligence
- Detect unusual outbound traffic from IoT devices

---

### 2. Exploitation of Default Credentials
Vulnerability:
Default or weak passwords on IoT device

Prevention:
- Change default credentials
- Enforce strong password policies
- Enable MFA where supported
- Restrict access to device management interface

Detection:
- Monitor login attempts and unusual access patterns
- DNS and firewall logging for suspicious connections

---

### 3. ARP Poisoning on Local Network
Vulnerability:
Unsecured local network and lack of ARP protection

Prevention:
- Segment network using guest or IoT VLANs
- Disable WPS on router
- Update router firmware
- Use endpoint detection tools

Detection:
- Identify ARP anomalies such as duplicate responses
- Monitor for sudden network instability
- Use tools like Snort or Suricata for detection

### 4. VPN Credential Capture
Vulnerability:
Weak credential handling and lack of strong authentication

Prevention:
- Enforce MFA for VPN access
- Use password managers instead of storing credentials locally
- Apply least privilege principles
- Use secure VPN protocols or ZTNA
- Enable full disk encryption

Detection:
- Monitor for unusual login behavior (location, time)
- Detect multiple failed login attempts
- Use endpoint detection for credential access activity

### 5. Access to Corporate Financial Systems
Vulnerability:
Weak access control and lack of segmentation

Prevention:
- Implement RBAC and least privilege access
- Use Zero Trust architecture
- Enforce device compliance checks
- Deploy EDR solutions
- Segment sensitive systems from general network access

Detection:
- Monitor SIEM and firewall logs for abnormal activity
- Detect unusual data transfers
- Identify suspicious user behavior in financial systems

## Key Takeaways
- IoT devices are a major entry point if not secured properly
- Network segmentation is critical in preventing lateral movement
- MFA and strong authentication reduce credential-based attacks
- Continuous monitoring is required to detect abnormal behavior early

## Files
- SmartHome_Breach_Report.pdf
