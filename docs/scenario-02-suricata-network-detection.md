# Scenario 02 — Network Activity Detection with Suricata

## Objective

Validate the integration between Suricata IDS and Wazuh by generating observable network activity from Kali Linux toward the Ubuntu endpoint.

## Environment

- **Traffic source:** Kali Linux
- **Monitored host:** Ubuntu Agent
- **Network IDS:** Suricata
- **Central platform:** Wazuh Manager and Dashboard

## Procedure

Network traffic was generated from Kali Linux toward the Ubuntu endpoint. Suricata inspected the traffic and wrote matching events to its logs.

```bash
nmap -sS 192.168.90.130
```

## Expected telemetry

- Source IP address
- Destination IP address
- Protocol
- Triggered Suricata signature
- Alert priority
- Suricata log entry
- Wazuh-correlated event

## Detection result

Suricata generated IDS events that were successfully forwarded to and displayed in Wazuh.

**Status:** Successfully detected.

## Security value

This integration adds network visibility to Wazuh's host-based monitoring capabilities and enables analysts to correlate endpoint and network events.

## MITRE ATT&CK mapping

The academic report did not assign a specific MITRE ATT&CK technique to this scenario. A precise mapping depends on the exact traffic or reconnaissance behavior generated.

## Screenshot

```text
assets/scenario-suricata.png
```
