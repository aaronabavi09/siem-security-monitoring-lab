# SIEM Security Monitoring Lab v1.0.0

## Initial stable release

This release presents a fully documented virtual security-monitoring laboratory built with **Wazuh**, **Suricata**, **Ubuntu**, **Kali Linux** and **VMware Workstation**.

The project demonstrates how endpoint logs and network-security events can be collected, centralized, correlated and investigated through a SIEM/XDR platform.

## Highlights

- Centralized security monitoring with Wazuh.
- Linux endpoint monitoring through the Wazuh Agent.
- Suricata IDS integration for network visibility.
- Real-time alert collection and visualization.
- Threat Hunting and security-event analysis.
- Five validated attack and detection scenarios.
- MITRE ATT&CK mapping for key adversary behaviors.
- Complete architecture, screenshots and technical documentation.

## Detection scenarios

1. File Integrity Monitoring.
2. Network-activity detection with Suricata.
3. SSH brute-force attack with Hydra.
4. Unauthorized administrator-account creation.
5. SSH access with the created account and privileged `sudo` activity.

## MITRE ATT&CK coverage

| Technique | ID | Demonstrated activity |
|---|---|---|
| Brute Force | T1110 | Repeated SSH authentication attempts |
| Create Account | T1136 | Creation of `backupadmin` |
| Account Manipulation | T1098 | Addition of `backupadmin` to the `sudo` group |
| Valid Accounts | T1078 | Successful SSH login using the created account |
| Sudo and Sudo Caching | T1548.003 | Privileged command execution |

## Environment

- Wazuh Server
- Ubuntu monitored endpoint
- Kali Linux attacker machine
- Suricata IDS
- VMware Workstation isolated network

## Academic context

Developed by **Aaron ABAVI** as part of the Professional Master's in Computer Science — Cybersecurity at the **Université du Québec à Chicoutimi (UQAC)**, under the supervision of **Mr. Fehmi Jaafar**.
