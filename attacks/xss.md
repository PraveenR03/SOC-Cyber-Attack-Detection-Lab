\# Cross-Site Scripting (XSS)



Target:

http://192.168.56.107/DVWA/vulnerabilities/xss\_r/



Payload:

<script>alert('XSS')</script>



Expected Outcome:

\- JavaScript executed in browser

\- HTTP payload logged

\- Alert indexed in Elasticsearch



