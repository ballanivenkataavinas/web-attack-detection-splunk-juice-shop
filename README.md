# ⭐  Web Attack Detection using Splunk SIEM

## 📌 Overview
This project demonstrates detection of web-based attacks such as SQL injection and login abuse using centralized log monitoring.

---

## 🧱 Lab Setup

- Web Application: OWASP Juice Shop  
- Platform: Docker  
- SIEM: Splunk  

---

## ⚔️ Attack Simulation

Simulated attacks include:

- SQL Injection  
- Login bypass attempts
- 
Example payload:
' OR 1=1 --

## 📡 Log Pipeline

Web Requests → juice.log → Splunk Forwarder → Splunk SIEM
## 🔍 Detection Queries (Splunk SPL)

```spl
index=* source="/home/employee/juice.log"
| search "/rest/user/login"
| stats count by host
index=* ("' OR 1=1" OR "admin' --")

📊 Analysis
Identified repeated login attempts
Detected suspicious input patterns
Monitored abnormal web activity

🎯 Outcome

Demonstrated detection of web attacks through SIEM-based log analysis.

🧠 Skills Demonstrated
Web Security Monitoring
SIEM Log Analysis
Attack Detection
SQL Injection Analysis
