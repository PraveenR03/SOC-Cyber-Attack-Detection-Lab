\# SQL Injection Attack



Target: DVWA (Security Level: Low)



URL:

http://192.168.56.107/DVWA/vulnerabilities/sqli/



Payloads Used:

\- ' OR '1'='1

\- 1' OR '1'='1

\- ' UNION SELECT NULL--



Expected Outcome:

\- Unauthorized database access

\- Suricata detects SQL Injection

\- Alert logged in eve.json

\- Filebeat forwards logs to Elasticsearch

\- Alert visible in Kibana



Evidence:

\- Screenshot: SQL injection success

\- Screenshot: Suricata alert

\- Screenshot: Kibana dashboard



