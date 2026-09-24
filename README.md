# Building a Virtual SOC Environment

A hands-on cybersecurity project focused on building and testing a small
Security Operations Center (SOC) environment using Splunk and Wazuh.

The project demonstrates Windows endpoint monitoring, log collection,
security event detection, file integrity monitoring, dashboard creation,
and basic incident investigation.

---

## 🚀 Project Overview

This project simulates a basic SOC environment where security events
generated on a Windows endpoint are monitored and investigated using
Splunk and Wazuh.

The lab was built using virtual machines and a Windows endpoint.

### Main objectives

- Collect Windows security logs
- Monitor Windows endpoint activity
- Detect failed authentication attempts
- Detect Windows account creation
- Monitor file integrity changes
- Create security dashboards
- Investigate security events
- Correlate detections between Splunk and Wazuh
- Practice basic SOC incident response

---

## 🏗️ Lab Architecture

```text
                 ┌─────────────────────┐
                 │     Windows 11      │
                 │      Endpoint       │
                 │                     │
                 │ Windows Security    │
                 │ Logs / File Changes  │
                 └──────────┬──────────┘
                            │
                ┌───────────┴───────────┐
                │                       │
                ▼                       ▼
       ┌────────────────┐      ┌────────────────┐
       │     Splunk     │      │     Wazuh      │
       │      SIEM      │      │     Manager    │
       │                │      │                │
       │ Log Analysis   │      │ Endpoint       │
       │ Dashboards     │      │ Monitoring     │
       └────────────────┘      │ FIM / Alerts   │
                               └───────┬────────┘
                                       │
                                       ▼
                               ┌────────────────┐
                               │ Wazuh Dashboard│
                               └────────────────┘
