# Scenario 05 — Valid Account Use and Privileged Activity

## Objective

Demonstrate how a newly created privileged account can be used for remote SSH access and administrative command execution, and validate Wazuh's visibility into the activity.

## Environment

- **Source:** Kali Linux
- **Target:** Ubuntu Agent
- **Account:** `backupadmin`
- **Monitored services:** SSH, PAM and `sudo`
- **Central platform:** Wazuh

## Procedure

The `backupadmin` account was used to establish an SSH connection from Kali Linux to the Ubuntu endpoint. Privileged commands were then executed with `sudo`.

```bash
ssh backupadmin@192.168.90.130
sudo whoami
```

## Expected telemetry

- Successful SSH authentication
- Use of a valid local account
- PAM session events
- `sudo` command execution
- Privilege-related alerts
- Chronological event correlation in Wazuh

## Detection result

Wazuh captured the successful remote login and the subsequent privileged activity.

**Status:** Successfully detected.

## MITRE ATT&CK mapping

| Technique | ID |
|---|---|
| Valid Accounts | T1078 |
| Sudo and Sudo Caching | T1548.003 |

## Security value

Monitoring successful logins and privileged commands provides essential evidence for post-compromise investigation and helps identify abuse of legitimate credentials.

## Screenshot

```text
assets/scenario-sudo.png
```
