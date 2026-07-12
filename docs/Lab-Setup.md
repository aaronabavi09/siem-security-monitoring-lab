# SIEM Security Monitoring Lab — Setup Summary

## Purpose

This document summarizes the laboratory topology and the main deployment stages.

## Virtual machines

| Machine | Role | Example IP |
|---|---|---|
| Wazuh Server | Manager, Indexer and Dashboard | 192.168.90.128 |
| Ubuntu Agent | Monitored endpoint, Wazuh Agent and Suricata | 192.168.90.130 |
| Kali Linux | Attack simulation | 192.168.90.132 |

## Core components

- VMware Workstation
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Wazuh Agent
- Suricata IDS
- Ubuntu Linux
- Kali Linux

## High-level deployment sequence

1. Create an isolated VMware virtual network.
2. Deploy the Wazuh Server virtual machine.
3. Install Wazuh Manager, Indexer and Dashboard.
4. Deploy the Ubuntu monitored endpoint.
5. Install and register the Wazuh Agent.
6. Install and configure Suricata on the Ubuntu endpoint.
7. Configure Wazuh to ingest relevant Suricata logs.
8. Deploy Kali Linux as the attack-simulation machine.
9. Validate network connectivity and agent status.
10. Execute the five detection scenarios.
11. Review alerts in Wazuh Dashboard and Threat Hunting.

## Notes

- IP addresses are examples from the academic laboratory and may be changed.
- Do not expose the lab directly to the public internet.
- Run attack simulations only in systems you own or are explicitly authorized to test.
- Product versions and installation commands should be verified against current official documentation before reproducing the lab.
