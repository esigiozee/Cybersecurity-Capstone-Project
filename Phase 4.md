Eseosa Igiozee

**Scenario 1: Unpatched RDP is Exposed to the Internet**



* **Description of the Vulnerability:** BlueKeep (CVE-2019-0708) and other known vulnerabilities can be exploited, as well as brute-force attacks, against Remote Desktop Protocol (RDP) services exposed to the internet without appropriate security measures or fixes.
* **Operating Systems/Versions Affected:** 
    * Windows Server 2008, 2012, 2016, 2019.
* **Risks of attempting to exploit**
    * Great chance of account lockout.
    * Maybe a system crash or loss of resources.
    * Detection by IDS/IPS systems.
* **Risk (what could you or a threat actor do upon successful exploitation)?**
    * Gain unauthorized access to the system.
    * Launch attacks on internal systems.
    * Acquire password hashes and crack them.
    * Move laterally into the network and access other systems.
    * Use tools like Hydra or Ncrack to perform brute-force attacks.
    * Capture and crack password hashes using tools like John the Ripper or Hashcat.
* **Remediation action**
    * Disable RDP if not needed.
    * Apply the latest security patches.
    * Use RDP gateways for remote access.
    * Enforce multi-factor authentication (MFA).
* **CVSS score**
    * 9.8 (Critical)

**Scenario 2: Web Application is Vulnerable to SQL Injection**



* **Description of the vulnerability**
    * SQL Injection vulnerabilities allow attackers to execute arbitrary SQL queries on the backend database by manipulating input fields.
* **Operating systems/versions affected**
    * Web applications with SQL backends (MySQL, MSSQL, Oracle, PostgreSQL).
* **Risks of attempting to exploit**
    * Database corruption.
    * Potential Denial of Service (DoS) attacks.
    * Detection by WAF or security monitoring tools.
        * Can be bypassed with regex if accessible.
            * Changing the case of the payload, using various encodings, substituting functions or characters, using an alternative syntax, and using line breaks or tabs.
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Compromise the database and exfiltrate data.
    * Execute arbitrary commands on the database server.
    * Bypass authentication and escalate privileges.
    * Access other systems connected to the database.
    * SQL injection through web forms, URL parameters, cookies.
* **Remediation action**
    * Use prepared statements and clean up inputs.
    * Use parameterized queries.
    * Patch and upgrade database systems frequently.
    * Put into place strict access restrictions.
* **CVSS score**
    * 9.0 (Critical)

**Scenario 3: Default password on Cisco admin portal**



* **Description of the vulnerability**
    * Using default credentials on Cisco admin portals allows attackers easy access to network devices.
* **Operating systems/versions affected**
    * Cisco network devices prior to a specific software release and with default credentials.
* **Risks of attempting to exploit**
    * Locked out of devices.
    * Direct access via web interface, SSH, or Telnet.
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Could authenticate with administrative privileges and arbitrarily change the configuration of Cisco Network Registrar.
    * Make backdoors and move to different parts of the network.
    * Alter network settings and intercept data.
    * Strong Password Policies: Enforcing password changes on initial setup.
    * Network Segmentation: Isolating management interfaces from the public network.
    * Attempt to log in using known default credentials.
    * If default credentials are unsuccessful, use brute-force or dictionary attacks.
* **Remediation action**
    * As soon as setup is done, change the default credentials.
    * Implement strong password policies.
    * Regularly audit device configurations.
* **CVSS score**
    * 10.0 (Critical)

**Scenario 4: Apache web server vulnerable to CVE-2019-0211 **



* **Description of the vulnerability**
    * Apache HTTP Server 2.4.17 to 2.4.38 is vulnerable to a local privilege escalation due to a flaw in the handling of the scoreboard shared memory area.
* **Operating systems/versions affected**
    * Apache HTTP Server 2.4.17 to 2.4.38 on Unix Operating systems.
* **Risks of attempting to exploit**
    * Crashing servers.
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Gain root access on the server.
    * Execute arbitrary commands and take control of the server.
    * Access sensitive data and move laterally.
* **Remediation action**
    * Update Apache to the latest or fixed version.
    * Implement security modules like ModSecurity.
    * Regularly audit and monitor server configurations.
* **CVSS score**
    * 7.8 (High)

**Scenario 5: Web server is exposing sensitive data**



* **Description of the vulnerability**
    * Misconfigured web servers can expose sensitive data such as configuration files, backup files, or sensitive documents.
* **Operating systems/versions affected**
    * Any web server with misconfigurations / Any OS like Windows Server, Linux, Unix.
* **Risks of attempting to exploit**
    * Data corruption or data loss.
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Data breach and identity theft.
    * Access password databases.
    * Exposure of intellectual property and sensitive documents.
    * Manipulation of configuration files to gain further access.
    * An attacker monitors network traffic,downgrades connections from HTTPS to HTTP, intercepts requests, and steals the user’s session cookie. The attacker then replays this cookie and hijacks the user’s (authenticated) session, accessing or modifying the user’s private data.
* **Remediation action**
    * Classify data processed, stored or transmitted by an application. 
        * Identify which data is sensitive according to privacy laws, regulatory requirements, or business needs.
    * Correct server configurations to restrict access to sensitive files.
    * Audit and fix permissions.
    * Use access control mechanisms to protect sensitive data.
    * Make sure to encrypt all sensitive data at rest.
* **CVSS score**
    * 7.5 (High)

**Scenario 6: Web application has broken access control**



* **Description of the vulnerability**
    * Broken access control vulnerabilities allow attackers to bypass authentication and authorization mechanisms to access restricted areas.
* **Operating systems/versions affected**
    * All known web servers, application servers, and web application environments are susceptible.
* **Risks of attempting to exploit**
    * Account potentially getting locked out
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Unauthorized access to restricted areas.
        * can potentially access, modify, or delete any data on the system.
    * Data leakage and privilege escalation.
        * Use captured session tokens or credentials to escalate privileges.
    * Manipulation of user data and settings.
* **Remediation action**
    * Implement strict access control mechanisms.
    * Regularly test and review access policies.
    * Ensure proper session management and token expiration.
    * Model access controls should enforce record ownership rather than accepting that the user can create, read, update, or delete any record.
    * Disable web server directory listing and ensure file metadata (e.g., .git) and backup files are not present within web roots.
* **CVSS score**
    * Depending on the impact it could be as low as 4 or 5 (medium) or as severe as 9 to 10 (Critical).

**Scenario 7: Oracle WebLogic Server vulnerable to CVE-2020-14882**



* **Description of the vulnerability**
    * Broken access control vulnerabilities allow attackers to bypass authentication and authorization mechanisms to access restricted areas.
* **Operating systems/versions affected**
    * Oracle WebLogic Server 10.3.6.0, 12.1.3.0, 12.2.1.3, 12.2.1.4.
* **Risks of attempting to exploit**
    * Server crash.
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * With Remote code execution access, an attacker can get into the WebLogic server. Due to the high privileges acquired, a malicious hacker can carry out any administrative action and take complete control over the application.
    * Remote code execution and server compromise.
    * Data breach and lateral movement.
    * bypass authentication of the console component with a simple HTTP GET request to a double encoded endpoint.
* **Remediation action**
    * Apply the latest patches from Oracle.
    * Restrict access to the WebLogic management console.
    * Regularly audit server configurations.
* **CVSS score**
    * 9.8 (Critical)

**Scenario 8: Misconfigured cloud storage (AWS security group misconfiguration, lack of access restrictions) **



* **Description of the vulnerability**
    * Misconfigured cloud storage services may result in unrestricted access, exposing confidential information.
* **Operating systems/versions affected**
    * AWS S3, Azure Blob Storage, Google Cloud Storage.
* **Risks of attempting to exploit**
    * Potential data loss or data corruption.
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Data exfiltration and public exposure.
    * Manipulation or deletion of stored data.
    * Pivot to other cloud services or resources.
    * access cloud-based data and ransom it.
    * Install digital skimming code onto the websites scripts to steal visitors sensitive information.
* **Remediation action**
    * Apply proper IAM policies and restrict public access.
    * Enable encryption.
    * Create, apply, and communicate strong security policies.
    * Monitor access logs and enforce least privilege.
    * Regularly audit cloud configurations.
* **CVSS score**
    * 8.5 (High)

**Scenario 9: Microsoft Exchange Server vulnerable to CVE-2021-26855**



* **Description of the vulnerability**
    * Microsoft Exchange Server is vulnerable to a Server-Side Request Forgery (SSRF) vulnerability, which allows attackers to send arbitrary HTTP requests and authenticate as the Exchange server.
* **Operating systems/versions affected**
    * Microsoft Exchange Server 2013, 2016, 2019.
* **Risks of attempting to exploit**
    * Server crashes.
    * Access to 3 other vulnerabilities:
        * CVE-2021-26857
        * CVE-2021-26858
        * CVE-2021-27065
* **Risk (what could you or a threat actor do upon successful exploitation)? **
    * Remote code execution and email compromise.
    * Data exfiltration and unauthorized access to mailboxes.
    * Pivot to other internal systems and escalate privileges.
* **Remediation action**
    * Install the necessary patches immediately.
    * Enable Exchange protection mechanisms.
    * Monitor for suspicious activities and review security configurations.
* **CVSS score**
    * 9.1 (Critical)
