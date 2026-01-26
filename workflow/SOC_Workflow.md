\# Secure Mini-SOC Workflow Documentation



\## 1. Virtualization Layer

All systems are deployed using Oracle VirtualBox. A Host-Only Network is configured to allow inter-VM communication while preventing internet exposure.



VM Allocation:

\- Kali Linux (Attacker): 4GB RAM

\- DVWA Server (Target): 4GB RAM

\- SOC VM (Suricata + ELK): 18GB RAM



Promiscuous Mode is enabled on the SOC VM to allow packet inspection of traffic not directly addressed to the SOC.



\## 2. Attack Generation

Attacks are launched manually from the Kali Linux browser against DVWA. These attacks include SQL Injection, Command Injection, XSS, Brute Force, and File Inclusion.



\## 3. Traffic Capture

Suricata runs in IDS mode using PCAP capture to monitor all traffic flowing between Kali and DVWA.



Captured traffic is analyzed in real time using both custom and Emerging Threat rules.



\## 4. Alert Generation

When malicious patterns are detected:

\- Suricata generates alerts

\- Alerts are written to `/var/log/suricata/eve.json`



\## 5. Log Shipping

Filebeat continuously monitors `eve.json` and automatically ships new log entries to Elasticsearch. No manual intervention is required.



\## 6. Indexing \& Storage

Elasticsearch parses incoming logs and stores them in Filebeat indices, making them searchable and structured.



\## 7. Visualization

Kibana retrieves indexed alerts from Elasticsearch and displays them in custom dashboards:

\- Alert frequency over time

\- Top attacking IPs

\- Attack type distribution

\- Severity breakdown



\## 8. Reporting \& Export

Dashboards and alerts can be exported as:

\- Screenshots

\- CSV/JSON reports

\- SOC incident summaries



\## Result

This workflow replicates a real SOC pipeline used in enterprise environments, from detection to analysis and reporting.



