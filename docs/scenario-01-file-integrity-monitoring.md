# Scenario 01 — File Integrity Monitoring

## Objective

Validate Wazuh's ability to detect the creation, modification and deletion of a monitored file on the Ubuntu endpoint.

## Environment

- **Monitored host:** Ubuntu Agent
- **Detection component:** Wazuh File Integrity Monitoring
- **Central platform:** Wazuh Manager and Dashboard

## Procedure

A test file was created inside a monitored directory, modified and then removed.

```bash
sudo touch /etc/test_fim.txt
echo "Test Wazuh FIM" | sudo tee -a /etc/test_fim.txt
sudo rm /etc/test_fim.txt
```

## Expected telemetry

- File-created event
- File-modified event
- File-deleted event
- File path
- Event timestamp
- Alert severity
- Monitored agent identity

## Detection result

Wazuh detected each change and forwarded the corresponding events to the central server.

**Status:** Successfully detected.

## Security value

File Integrity Monitoring helps identify unauthorized changes that may indicate compromise, malware installation, configuration tampering or malicious persistence.

## MITRE ATT&CK mapping

The academic report did not assign a specific MITRE ATT&CK technique to this scenario. Any mapping added later should be based on the exact adversary behavior being emulated rather than the monitoring control itself.

## Screenshot

```text
assets/scenario-fim.png
```
