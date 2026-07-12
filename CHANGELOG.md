# Changelog

All notable changes to the **SIEM Security Monitoring Lab** project are documented in this file.

The format follows the principles of Keep a Changelog, and the project uses semantic versioning.

## [1.0.0] - 2026-07-12

### Added

- Initial public release of the SIEM Security Monitoring Lab.
- Wazuh Manager, Indexer and Dashboard deployment.
- Ubuntu monitored endpoint with Wazuh Agent.
- Suricata IDS integration for network-event monitoring.
- Kali Linux attack-simulation machine.
- File Integrity Monitoring scenario.
- Suricata network-activity detection scenario.
- SSH brute-force detection scenario using Hydra.
- Unauthorized account creation and account manipulation scenario.
- SSH login and privileged `sudo` activity scenario.
- MITRE ATT&CK mapping for detected authentication and privilege-related activity.
- Threat Hunting and alert-analysis screenshots.
- Laboratory architecture and security-monitoring pipeline diagrams.
- Academic report and scenario documentation.

### Detection coverage

- File creation, modification and deletion.
- Network IDS alerts.
- Repeated SSH authentication failures.
- Unauthorized local-account creation.
- Addition of an account to the `sudo` group.
- Successful SSH login with a valid account.
- Execution of privileged commands with `sudo`.

### Known limitations

- Single monitored Linux endpoint.
- No Windows endpoint or Sysmon integration.
- No automated Active Response workflow.
- Limited custom Suricata rules.
- Resource consumption may increase with vulnerability-detection and indexing features.
