# 🛡️ DNS Threat Monitoring using Splunk Enterprise


---

# 📌 Project Overview

This project demonstrates the implementation of a DNS Threat Monitoring solution using **Splunk Enterprise** for Security Operations Center (SOC) monitoring.

The objective is to collect, analyze, and investigate DNS traffic using Splunk Search Processing Language (SPL). Multiple reports, dashboards, and detection rules were developed to identify suspicious DNS activities including excessive DNS requests, abnormal client behavior, and potentially malicious domain queries.

The project simulates the workflow of a Tier-1 SOC Analyst by transforming raw DNS logs into actionable security insights through visualization, reporting, and investigation.

> **Disclaimer**
>
> This project was performed using a simulated DNS log dataset within a controlled lab environment for educational purposes only.

---

# 🎯 Objectives

- Import DNS security logs into Splunk Enterprise
- Verify successful indexing
- Analyze DNS traffic using SPL
- Monitor DNS activity
- Identify high-volume DNS clients
- Detect suspicious domains
- Create analytical reports
- Build interactive dashboards
- Perform incident investigations
- Simulate a SOC analyst workflow

---

# 🏗️ Lab Environment

| Component | Details |
|------------|----------|
| Operating System | Windows 10 |
| SIEM Platform | Splunk Enterprise |
| Dataset | DNS Security Logs |
| Log Format | CSV |
| Source Type | csv |
| Index | main |

---

# 📂 Dataset Information

The dataset contains approximately **5,000 DNS events**.

Each log contains:

- Timestamp
- Source IP
- Destination DNS Server
- DNS Query
- Query Type
- Response IP
- DNS Status

---

# 🛠️ Technologies Used

- Splunk Enterprise
- SPL (Search Processing Language)
- Windows
- DNS Logs
- CSV Dataset

---

# ⚙️ Project Implementation

## Step 1 – Splunk Installation

Installed Splunk Enterprise on Windows.

---

## Step 2 – Data Import

Imported DNS security logs into Splunk.

Verified successful indexing.

---

## Step 3 – Log Verification

Verified events using:

```spl
index=main source="dns_security_logs.csv"
```

---

## Step 4 – DNS Analysis

Performed multiple SPL searches including:

- Total DNS Requests
- Top Queried Domains
- DNS Status
- Source IP Analysis
- Traffic Timeline
- Suspicious Domain Detection

---

## Step 5 – Reports

Created multiple analytical reports.

### Excessive DNS Requests

```spl
index=main source="dns_security_logs.csv"
| stats count by Source_IP
| where count>100
```

---

### DNS Status Monitoring

```spl
index=main source="dns_security_logs.csv"
| stats count by Status
```

---

### Top Queried Domains

```spl
index=main source="dns_security_logs.csv"
| top Query limit=20
```

---

## Step 6 – Dashboard

Developed an interactive SOC dashboard containing:

- Total DNS Requests
- Top Queried Domains
- Most Active Source IPs
- DNS Status
- DNS Traffic Timeline

---

## Step 7 – Detection Rules

Implemented detection logic for:

- High DNS activity
- Suspicious domains
- Failed DNS lookups
- Most active hosts

---

## Step 8 – Incident Investigation

Performed investigation to identify:

- High-volume source IPs
- Queried domains
- DNS response status
- Timeline of DNS activity

---

# 📊 Dashboard

The dashboard includes:

- DNS Request Counter
- Top Domains
- Source IP Distribution
- DNS Status Analysis
- DNS Traffic Timeline

---

# 🚨 Detection Use Cases

## High DNS Requests

Identify hosts generating excessive DNS traffic.

## Suspicious Domains

Identify potentially malicious domains.

## Failed DNS Queries

Detect DNS resolution failures.

## Traffic Analysis

Monitor DNS request trends.

---

# 📈 Results

✔ Successfully indexed DNS logs

✔ Developed SPL queries

✔ Created reports

✔ Built security dashboards

✔ Performed incident investigation

✔ Simulated SOC monitoring workflow

---

# 🧠 Skills Demonstrated

- Splunk Enterprise
- SIEM Operations
- DNS Analysis
- SPL Query Development
- Dashboard Development
- Security Reporting
- Threat Hunting
- Blue Team Operations
- Incident Investigation

  
---

# 🚀 Future Enhancements

- Universal Forwarder Integration
- Sysmon Integration
- Threat Intelligence Feeds
- VirusTotal Lookup
- Email Alerting
- MITRE ATT&CK Mapping
- DNS Tunneling Detection
- Real-time Log Collection

---

# 📚 Conclusion

This project demonstrates how Splunk Enterprise can be leveraged to monitor DNS traffic, identify suspicious behavior, and support SOC investigations through effective log analysis, dashboard creation, reporting, and threat detection.

The project provides practical experience with SIEM operations and Blue Team monitoring techniques commonly used in enterprise security environments.
