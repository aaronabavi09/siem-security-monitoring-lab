# Scenario 04 — Unauthorized Account Creation and Manipulation

## Objective

Simulate persistence by creating a new local account and granting it administrative privileges.

## Environment

- **Monitored host:** Ubuntu Agent
- **Created account:** `backupadmin`
- **Privileged group:** `sudo`
- **Central platform:** Wazuh

## Procedure

A new user account was created on the monitored endpoint and added to the `sudo` group.

```bash
sudo adduser backupadmin
sudo usermod -aG sudo backupadmin
```

## Expected telemetry

- New local-user creation
- System account database modification
- Group membership change
- Assignment of administrative privileges
- Wazuh alerts containing user and event details

## Detection result

Wazuh detected the account creation and the subsequent privilege-related group modification.

**Status:** Successfully detected.

## MITRE ATT&CK mapping

| Technique | ID |
|---|---|
| Create Account | T1136 |
| Account Manipulation | T1098 |

## Security value

Unauthorized privileged-account creation is a common persistence technique. Rapid detection helps administrators investigate and contain post-compromise activity.

## Screenshot

```text
assets/scenario-account.png
```
