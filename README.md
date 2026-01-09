# projects-dos-incident-report.md
NIST and CSF Incident  report
### 1. DoS Incident Report Analysis Using NIST CSF
- Analyzed a real-world Denial of Service (DoS) attack scenario involving an ICMP flood.
- Applied the NIST Cybersecurity Framework to identify risks, protections, detection methods, response actions, and recovery steps.
- Demonstrates incident reporting, risk management, and network security planning.
- **Tools/Concepts**: NIST CSF, ICMP protocols, firewall rules, IDS/IPS
- [View Full Report](projects/dos-incident-report.md)

### 2. Network Security Audit Using Wireshark
- Captured and analyzed network traffic using Wireshark.
- Identified potential security issues such as unencrypted protocols and unusual traffic patterns.
- Documented findings in a professional audit report.
- **Tools**: Wireshark, tcpdump
- [View Report & Screenshots](projects/wireshark-audit.md)

### 3. Incident Response Playbook (Phishing Attack Simulation)
- Developed a step-by-step incident response playbook based on the NIST framework.
- Covered detection, containment, eradication, recovery, and lessons learned for a simulated phishing incident.
- **Framework**: NIST 800-61
- [View Playbook](projects/phishing-playbook.md)

### 4. Python Security Automation Script
- Wrote Python scripts to parse logs, check password strength, and automate repetitive tasks.
- **Skills Demonstrated**: Automation in security workflows
- [View Code on GitHub](projects/python-scripts/)

### 5. SQL Queries for Security Investigations
- Used SQL to query mock security databases for suspicious activity.
- [View Sample Queries](projects/sql-queries.md)

### 6. Linux Security Commands & File Analysis
- Demonstrated Linux CLI proficiency for security tasks.
- [View Commands & Examples](projects/linux-commands.md)
- rkdown# DoS Incident Report Analysis: ICMP Flood Attack

**Author:** Byron Bates  
**Date:** January 2026  
**Course:** Google Cybersecurity Professional Certificate – Connect and Protect: Networks and Network Security  

## Summary
A multimedia company providing web design, graphic design, and social media marketing services experienced a **Denial of Service (DoS) attack**. The internal network was compromised for two hours due to a flood of incoming ICMP packets, preventing normal traffic from accessing network resources.

The incident management team blocked incoming ICMP packets, took non-critical services offline, and restored critical services. Investigation revealed the attacker exploited an unconfigured firewall to send excessive ICMP pings, overwhelming the network.

Post-incident, the team implemented:
- A firewall rule to rate-limit incoming ICMP packets
- Source IP verification to detect spoofed addresses
- Network monitoring for abnormal patterns
- An IDS/IPS system to filter suspicious ICMP traffic

This report applies the **NIST Cybersecurity Framework (CSF)** to analyze the incident and recommend improvements to network security.

## NIST CSF Analysis

### Identify
Security risks arise from gaps in internal audits. The unconfigured firewall allowed unrestricted ICMP traffic, a common DoS vulnerability.

**Recommendations:**  
Conduct regular audits of networks, systems, devices, firewalls, and access privileges. Identify vulnerabilities like open ICMP ports or missing rate-limiting to prioritize risks.

### Protect
Safeguards protect assets through policies, procedures, training, and tools.

**Implemented/Actions Taken:**  
- New firewall rule limiting ICMP packet rates  
- Source IP verification against spoofing  
- IDS/IPS deployment to filter suspicious ICMP traffic  

**Additional Recommendations:**  
- Implement access controls and least privilege on firewalls  
- Provide employee training on network security best practices  
- Enforce policies disabling unnecessary ICMP where possible

### Detect
Early detection requires monitoring to identify incidents quickly.

**Implemented/Actions Taken:**  
Network monitoring software now detects abnormal traffic patterns (e.g., sudden ICMP spikes).

**Additional Recommendations:**  
- Deploy continuous SIEM tools for real-time log correlation  
- Set alerts for high-volume ICMP or unusual sources  
- Improve anomaly detection for faster response

### Respond
Response actions contain, neutralize, and analyze incidents while improving processes.

**Actions Taken During Incident:**  
- Blocked incoming ICMP packets  
- Stopped non-critical services to restore critical ones  
- Investigated root cause (unconfigured firewall)  

**Additional Recommendations:**  
- Develop playbooks for DoS incidents, including escalation and communication  
- Perform post-response analysis to document lessons learned  
- Coordinate with ISPs for upstream filtering in future attacks

### Recover
Recovery restores systems to normal operation and repairs damage.

**Actions Taken:**  
Critical network services were fully restored after two hours.

**Additional Recommendations:**  
- Test backups and recovery plans regularly  
- Patch vulnerabilities identified (e.g., firewall configuration)  
- Conduct post-incident reviews to update resilience  
- Restore non-critical services gradually with monitoring

## Conclusion & Reflections
This DoS attack highlights ICMP risks when firewalls lack proper configuration. Applying NIST CSF provides a structured approach to turn the incident into stronger security.

By enhancing identification through audits, protection via controls, detection with monitoring, response with playbooks, and recovery planning, the organization can better prevent and mitigate future DoS attacks.

This analysis demonstrates proactive risk management and incident handling—key skills for any cybersecurity role.

**Skills Demonstrated:** Network protocol analysis (ICMP), NIST CSF application, incident reporting, vulnerability assessment.

