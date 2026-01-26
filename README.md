\# Secure Mini-SOC: End-to-End IDS/IPS Pipeline using Suricata and ELK



\## Project Overview

This project implements a fully functional Security Operations Center (SOC) pipeline capable of detecting, analyzing, and visualizing real cyberattacks in a controlled virtual lab. The system integrates Suricata IDS, Filebeat, Elasticsearch, and Kibana to provide real-time detection and centralized security monitoring.



\## Architecture

\- Attacker: Kali Linux

\- Target: Ubuntu Server with DVWA

\- SOC/SIEM: Ubuntu Server running Suricata + ELK Stack



All virtual machines are connected using a Host-Only Network to isolate the lab while allowing full packet visibility.



\## Key Features

\- Network-based intrusion detection using Suricata

\- Real attack simulation (SQLi, XSS, Command Injection, Brute Force)

\- Centralized log ingestion using Filebeat

\- Real-time alert indexing in Elasticsearch

\- Custom Kibana dashboards for SOC monitoring

\- Alert export capability for reporting and evidence



\## Tools Used

\- Suricata IDS

\- Filebeat

\- Elasticsearch

\- Kibana

\- DVWA

\- Kali Linux

\- Oracle VirtualBox



\## Repository Structure



