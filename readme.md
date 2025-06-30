# P0rtFinder

**P0rtFinder** is a powerful and customizable Python-based port scanning tool designed for cybersecurity professionals, penetration testers, and enthusiasts. It helps identify open TCP/UDP ports and associated services on a target system. P0rtFinder also integrates the Nmap Scripting Engine (NSE), allowing users to run advanced security scripts for vulnerability detection directly from the tool.

---

## **🚀 Features**

-  **Port Scanning**: Efficiently scan TCP and UDP ports within a specified range.
-  **Service Detection**: Identify and display common services running on the open ports.
-  **Nmap NSE Integration**: Leverage specialized scripts to identify weaknesses and vulnerabilities in various platforms.
-  **Stylish Output**: Enjoy a clean, readable output with color-coded results and formatted tables.
---

## **🛠️ Use Cases**
- ✅ Network reconnaissance in ethical hacking

- ✅ Port visibility audits during red/blue teaming

- ✅ Vulnerability detection using NSE scripts

- ✅ Educational tool for learning about network services

---

## **🌐 Supported Platforms & Services**

- **WordPress (CMS)**
- **Joomla (CMS)**
- **Drupal (CMS)**
- **Apache (Web Server)**
- **MySQL (Database)**
- **Cloudflare (CDN)**

---

## **📦 Installation**

To get started with P0rtFinder, clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/AyushKr41/P0rtFinder.git
cd P0rtFinder
pip install -r requirements.txt
```

---

## **🎯 Usage**
Run P0rtFinder with the following command:
```bash
python P0rtFinder.py <target> [options]
```
Options:

**- target: The IP address or hostname of the target to scan.**

**- p START END, --ports START END: Define the range of ports to scan (default: 1-100).**

**- P {tcp,udp}, --protocol {tcp,udp}: Specify the protocol to scan (default: tcp).**

**- s `<script>`, --scripts `<script>`: Specify NSE scripts to run against the target.**

**- v, --verbose: Enable verbose output for more detailed information.**

---

## **🖥️ Example Commands**
To scan TCP ports from 1 to 100 on a target IP address:
```bash
python P0rtFinder.py example.com -p 1 100 -P tcp
```
```bash
python P0rtFinder.py 0.0.0.0 -p 1 100 -P tcp
```
To scan WordPress site or any other with specific NSE scripts:
```bash
python P0rtFinder.py <wordpress-site> -p 80 443 -s http-wordpress-enum http-wordpress-brute

```
---
## 📜 **NSE Scripts for Specific Services**
1.   **WordPress (CMS)**
```bash
http-wordpress-enum: Enumerates WordPress users.

http-wordpress-brute: Brute-forces WordPress login credentials.

http-enum: Scans for common web application directories, including those used by WordPress.

http-vuln-cve2017-1001000: Detects a remote code execution vulnerability (CVE-2017-1001000).

http-sql-injection: Scans for SQL injection vulnerabilities on WordPress.
```
2. **Joomla (CMS)**
```bash
http-joomla-brute: Attempts to brute-force Joomla login.

http-enum: Scans for directories used by Joomla.

http-sql-injection: Scans Joomla for SQL injection vulnerabilities.

http-vuln-cve2015-8562: Checks for the Joomla RCE vulnerability (CVE-2015-8562).

```
3. **Drupal (CMS)**
```bash
http-drupal-enum: Enumerates users on a Drupal site.

http-drupal-brute: Attempts to brute-force Drupal login.

http-vuln-cve2014-3704: Detects SQL injection vulnerability in Drupal (CVE-2014-3704).
```
4. **Apache (Web Server)**
```bash
http-apache-negotiation: Tests Apache content negotiation misconfigurations.

http-apache-server-status: Retrieves Apache server status page.

http-enum: Identifies common directories in Apache-hosted web applications.

http-slowloris-check: Tests for Slowloris DoS vulnerability.
```
5. **MySQL (Database)**
```bash
mysql-brute: Attempts to brute-force MySQL login credentials.

mysql-empty-password: Checks for MySQL accounts with empty passwords.

mysql-users: Enumerates MySQL users.

mysql-vuln-cve2012-2122: Detects a MySQL authentication bypass vulnerability (CVE-2012-2122).
```
6. **Cloudflare (CDN)**
```bash
http-cloudflare-resolve: Attempts to bypass Cloudflare by resolving the origin IP of a website.

http-dns-brute: Brute-forces subdomains, potentially exposing services not protected by Cloudflare.

dns-brute: Similar to http-dns-brute, but at the DNS level.
```

---
## 📜**Running Multiple Scripts**
You can specify multiple scripts for testing different CMS, servers, and databases by providing a space-separated list of scripts in the -s argument.
```bash
python P0rtFinder.py <target-site> -p 80 443 -s http-wordpress-enum http-enum http-sql-injection
```
---
## **⚖️ Legal Considerations**
P0rtFinder is intended for educational and authorized penetration testing purposes only.

By using this tool, you agree to the following:

✅ You will not use P0rtFinder to scan, probe, or interact with systems or networks without explicit permission from the owner.

✅ You are solely responsible for any misuse or unauthorized activity performed using this tool.

✅ The developer is not liable for any damage, legal consequences, or misuse resulting from the use of this project.

>❗ Always obtain proper authorization before scanning any network or device. Unauthorized scanning is a violation of privacy laws and can be considered illegal hacking under local or international law (e.g., the Computer Fraud and Abuse Act in the U.S. or the IT Act in India).

---
## **🛡️ Ethical Usage**
- Use in lab environments, CTFs, bug bounty, or client-approved pentests.
- Respect all terms of service and network usage policies.
---
## **🤝 Contributing**
Contributions are welcome! Feel free to submit pull requests or open issues to enhance the tool. Your feedback and contributions help improve Agniscan.

---

## **🙌 Credits**

    Developed by: Ayush Kumar
    Linkedin: https://www.linkedin.com/in/ayush-kumar-ak4422 

P0rtFinder is intended for security professionals to scan and assess network vulnerabilities. Use it responsibly and ensure you have permission before scanning any network.

---