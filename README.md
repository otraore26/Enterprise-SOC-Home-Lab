# Enterprise-SOC-Home-Lab
A hands-on Enterprise SOC Home Lab featuring Security Onion, pfSense, Active Directory, Windows Server 2025, Windows 11, and Splunk Enterprise for centralized logging, network monitoring, threat detection, and security operations.
# Overview

This project documents the development of a complete Enterprise Security Operations Center (SOC) Home Lab designed to simulate a real-world corporate environment. The lab combines centralized log management, Active Directory administration, network security monitoring, intrusion detection, firewall management, and threat hunting capabilities.

The objective of this project is to gain hands-on experience with technologies commonly used by Security Analysts, SOC Analysts, Incident Responders, and Security Engineers. The environment allows for the generation, collection, analysis, and investigation of security events across multiple systems while following industry-standard security monitoring practices.

This lab serves as a platform for testing detection rules, investigating security incidents, analyzing Windows authentication events, monitoring network traffic, and developing threat hunting skills.

---

# Environment

| Technology | Purpose |
|------------|---------|
| Splunk Enterprise | SIEM and centralized log management |
| Splunk Universal Forwarder | Endpoint log collection |
| Windows Server 2025 | Active Directory Domain Controller |
| Active Directory Domain Services | Identity and Access Management |
| DNS Server | Name Resolution |
| Windows 11 Enterprise | Domain-Joined Workstation |
| Security Onion | Network Security Monitoring |
| Zeek | Network Traffic Analysis |
| Suricata | Intrusion Detection System |
| Wazuh | Endpoint Detection and Monitoring |
| pfSense | Firewall and Network Segmentation |
| Oracle VirtualBox | Virtualization Platform |
| PowerShell | Administrative Automation |
| SPL | Security Analytics and Searches |

---

# SOC Architecture

```text
                          Internet
                              |
                              |
                       +--------------+
                       |   pfSense    |
                       |  Firewall    |
                       +------+-------+
                              |
         ---------------------------------------------
         |                                           |
         |                                           |
+--------+---------+                    +------------+-----------+
| Security Onion   |                    | Splunk Enterprise      |
| IDS / NSM        |                    | SIEM Platform          |
| Zeek             |                    | Central Log Storage    |
| Suricata         |                    | Search & Reporting     |
+--------+---------+                    +------------+-----------+
         |                                           |
         |                                           |
         ---------------------------------------------
                              |
                              |
                 +------------+-----------+
                 | Windows Server 2025    |
                 | Active Directory       |
                 | Domain Controller      |
                 +------------+-----------+
                              |
                              |
                 +------------+-----------+
                 | Windows 11 Enterprise  |
                 | Domain Joined Endpoint |
                 +------------------------+
```

---

# Lab Components

## 🏢 Active Directory Environment

The lab includes a Windows Server 2025 Domain Controller configured with:

- Active Directory Domain Services (AD DS)
- DNS Services
- Domain User Accounts
- Organizational Units (OUs)
- Authentication Policies
- Group Management

The Windows 11 workstation is joined to the domain to simulate a corporate endpoint environment.

---

## 📊 Splunk Enterprise SIEM

Splunk Enterprise serves as the centralized Security Information and Event Management (SIEM) platform.

### Functions

- Log Aggregation
- Event Correlation
- Authentication Monitoring
- Dashboard Creation
- Security Investigations
- Threat Detection
- Search & Reporting

### Data Sources

- Windows Security Logs
- Windows System Logs
- Active Directory Events
- DNS Events
- Firewall Logs
- Security Onion Alerts

---

## 📡 Splunk Universal Forwarders

Splunk Universal Forwarders are installed on:

### Windows Server 2025
- Security Logs
- System Logs
- Active Directory Events

### Windows 11 Enterprise
- Security Logs
- Authentication Events
- Endpoint Activity

The forwarders securely transmit logs to Splunk Enterprise for centralized analysis.

---

## 🔥 pfSense Firewall

pfSense provides perimeter security and network visibility.

### Responsibilities

- Firewall Rule Management
- Traffic Filtering
- Network Segmentation
- VPN Services
- Log Generation
- Security Monitoring

Firewall logs can be forwarded to Splunk for investigation and correlation.

---

## 🧅 Security Onion

Security Onion provides network security monitoring and threat detection capabilities.

### Components

#### Zeek

Used for:

- Network Traffic Analysis
- Connection Monitoring
- DNS Monitoring
- HTTP Analysis

#### Suricata

Used for:

- Intrusion Detection
- Signature-Based Detection
- Alert Generation
- Threat Monitoring

#### Wazuh

Used for:

- Endpoint Monitoring
- File Integrity Monitoring
- Security Event Collection

---

# Scenarios Completed
