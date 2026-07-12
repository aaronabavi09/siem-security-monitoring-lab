# Scenario 03 — SSH Brute-Force Detection

## Objective

Simulate a password-guessing attack against the SSH service of the Ubuntu endpoint and validate Wazuh's ability to detect repeated authentication failures.

## Environment

- **Attacker:** Kali Linux
- **Target:** Ubuntu Agent
- **Attack tool:** Hydra
- **Monitored logs:** Linux authentication logs
- **Central platform:** Wazuh

## Procedure

Hydra was used from Kali Linux to perform repeated SSH authentication attempts against the monitored endpoint.

```bash
hydra -l agentuser -P passwords.txt ssh://192.168.90.130
```

Use attack tools only in an authorized laboratory environment.

## Expected telemetry

- Repeated SSH login attempts
- Authentication failures
- PAM and SSH log entries
- Source IP address
- Target account
- Correlated Wazuh alerts

## Detection result

The failed authentication attempts were collected from the Linux authentication logs and correlated by Wazuh.

**Status:** Successfully detected.

## MITRE ATT&CK mapping

| Technique | ID |
|---|---|
| Brute Force | T1110 |

## Security value

Detecting repeated login failures allows defenders to identify credential attacks before an attacker successfully compromises an account.

## Screenshot

```text
assets/scenario-hydra.png
```
