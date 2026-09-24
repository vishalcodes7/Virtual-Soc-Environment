# 🛡️ Building a Virtual SOC Environment

A hands-on cybersecurity project focused on building and testing a small
Security Operations Center (SOC) environment using **Splunk** and **Wazuh**.

The project demonstrates Windows endpoint monitoring, security log analysis,
security event detection, File Integrity Monitoring (FIM), dashboard creation,
incident investigation, and basic incident response.

---

## 🎯 Project Objectives

- Collect Windows security logs
- Monitor a Windows endpoint
- Detect failed authentication attempts
- Detect Windows account creation
- Monitor file integrity changes
- Investigate security alerts
- Create SOC dashboards
- Correlate security events between Splunk and Wazuh
- Practice basic incident response

---

## 🏗️ Lab Architecture

```text
                    Windows 11
                     Endpoint
                        │
             ┌──────────┴──────────┐
             │                     │
             ▼                     ▼
          Splunk                  Wazuh
           SIEM                  Manager
             │                     │
             │                     ▼
             │               Wazuh Dashboard
             │
             ▼
       Splunk Dashboard


🛠️ Technologies Used
Technology	Purpose
Splunk	Log collection, searching and analysis
Wazuh	Endpoint monitoring and security detection
Windows 11	Monitored endpoint
Ubuntu	Splunk server
VirtualBox	Virtualization
PowerShell	Controlled security-event generation
Windows Event Logs	Security telemetry


🔎 Security Incidents Tested
1. Failed Windows Login

Windows Event ID: 4625

A controlled failed authentication scenario was generated on the
Windows endpoint.

The activity was detected and investigated using both Splunk and Wazuh.

Wazuh Rule: 60122

Evidence

2. File Integrity Monitoring

A test file was modified on the Windows endpoint:

C:\Users\Public\fim-test.txt

Wazuh detected the modification using real-time File Integrity Monitoring.

Wazuh Rule: 550

The alert identified changes including:

File size
Modification time
MD5
SHA1
SHA256
Evidence

3. Windows Account Creation

A temporary Windows test account was created to generate a security event.

Windows Event ID: 4720

The event was detected and investigated using Splunk and Wazuh.

The temporary test account was removed after testing.

Evidence


📊 SOC Dashboards
Splunk Dashboard

The Splunk dashboard contains:

Failed Windows Login
Windows Account Creation
Windows Security Events Over Time


Wazuh Dashboard

The Wazuh dashboard contains:

SOC Security Events Over Time
Failed Windows Logins
Windows Account Creations
File Integrity Changes


🔄 SOC Investigation Workflow
Generate Security Event
          ↓
Collect Endpoint Logs
          ↓
Detect Security Event
          ↓
Investigate Alert
          ↓
Correlate Evidence
          ↓
Document Incident
          ↓
Basic Incident Response


🧪 Skills Demonstrated
SIEM log analysis
Splunk SPL
Windows Security Event analysis
Wazuh alert investigation
File Integrity Monitoring
Endpoint monitoring
Dashboard creation
Security event correlation
Basic incident response
Cybersecurity documentation


📄 Project Report

The complete project report is available in this repository:

Virtual-SOC-Project-Report.pdf


⚠️ Disclaimer

This project was created for educational and cybersecurity lab purposes.

All security events were generated in a controlled environment using
test activities and temporary accounts.

No unauthorized systems were targeted.


👨‍💻 Author

Vishal Bhambhana

BCA Cybersecurity Student
