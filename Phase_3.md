Eseosa Igiozee

In phase 1, the goal was to build as robust a profile on the target, Artemis as possible. The deliverable covered 15 tools and methods that would be used to accomplish this task of reconnaissance. For phase 2, the goal was to identify at least 5 tools and techniques to be used to perform host discovery and enumeration. For phase 3, the goal is to now Identify the tools and techniques to be used to scan for vulnerabilities. Listed below will be the tools that will be used to perform vulnerabilities, how they will be used and screenshots of the tools showing configuration options and settings



* Tenable Nessus
    * Tenable Nessus is a robust vulnerability scanner known for its huge plugin library and accurate vulnerability assessments. It assists in identifying vulnerabilities, misconfigurations, and compliance issues across a variety of devices and applications.
    * How they get used:
        * **Setup & Configuration:** Install Nessus and configure it to scan Artemis’ network. Create a new scan, select a scan template (e.g., Basic Network Scan), and define the target IP ranges.
        * **Scanning:** Execute the scan to detect vulnerabilities, misconfigurations, and compliance issues. Nessus can scan various network devices, servers, and applications.
        * **Analysis**: Review the scan results in Nessus' dashboard. Prioritize vulnerabilities based on severity and follow the remediation steps provided.
    * Pros
        * Extensive plugin library and regular updates.
        * User-friendly interface with detailed reports.
        * Strong compliance and audit features.
    * Cons
        * Requires a paid subscription for full functionality.
        * Can be resource-intensive during scans.
  
![Nessus 1](https://github.com/user-attachments/assets/0c18a0d1-393e-4c90-9f50-c4663ac1819b)
![Nesssus 2](https://github.com/user-attachments/assets/8802a394-3f0b-4848-b952-63caccb52cb2)
![Nesssus 3](https://github.com/user-attachments/assets/7c752b69-0317-4029-9595-711b202d4359)


* OpenVAS
    * is a free and open-source vulnerability scanner made to find possible security holes in various network services. It uses a database of known vulnerabilities to provide detailed information about misconfigurations, outdated software, and exploitable flaws.
    * How they get used:
        * **Setup & Configuration:** Set up OpenVAS with updated vulnerability databases. Configure scanning tasks based on network segments.
        * **Vulnerability Scanning:** Perform a comprehensive scan to detect known vulnerabilities across network systems, focusing on outdated services and misconfigurations.
        * **Reporting:** Analyze scan results through detailed reports that categorize and prioritize vulnerabilities.
    * Pros
        * Free and open-source.
        * Regularly updated database of Network Vulnerability Tests.
        * Extensive configuration options.
    * Cons
        * Requires more setup and maintenance than some commercial tools.
        * User interface is less intuitive than Nessus.
      
![openvas1](https://github.com/user-attachments/assets/c6b07e7e-022c-41af-8d4f-2746d20c0e17)
![openvas2](https://github.com/user-attachments/assets/e8d2e2c7-38e2-4dc0-be8d-ccc70721b837)

* Burp Suite
    * Burp Suite is a well-known web application security testing tool that offers a complete solution for mapping, scanning, and exploiting web applications.
    * Usages:
        * **Configuration:** Configure Burp to intercept traffic from web applications deployed by Artemis.
        * **Automated Scanning**: Use the scanner module to automatically detect and report on vulnerabilities.
        * **Manual Testing:** Utilize the proxy tool to perform manual exploitation of vulnerabilities like SQL injections or XSS.
    * Pros
        * Comprehensive web application testing tool.
        * Supports both automated and manual testing methods.
    * Cons
        * Steep learning curve for new users.
        * Primarily focused on web applications, not network-level vulnerabilities.

![Burp1](https://github.com/user-attachments/assets/16ec834e-bd01-4cad-8d40-f2073cd58eec)
![Burp2](https://github.com/user-attachments/assets/5b7eb0d0-fc19-432f-8a24-d15b907dd0e3)
![Burp3](https://github.com/user-attachments/assets/28a5a2d1-cab6-4a37-9a22-252f6fc76b9f)
      
* Qualys
    * Qualys is a cloud-based vulnerability management tool that provides comprehensive scanning and detailed reporting for identifying security vulnerabilities, compliance issues, and configuration errors across IT environments.
    * Usage:
        * **Web application scanning: **Secure web applications with end-to-end protection. Qualys WAS is a robust solution for continuous web app discovery and detection of vulnerabilities and misconfigurations.
        * **Asset management: **Find and manage cybersecurity risks in IT assets. Qualys CSAM continuously inventories assets, applies business criticality and risk context, detects security gaps, and responds with appropriate actions to mitigate risk.
        * **Vulnerability Management, Detection and Response: **Discover, assess, prioritize, and patch critical vulnerabilities in real-time and across your global hybrid-IT landscape
    * Pros
        * Comprehensive Vulnerability Database:
        * User-Friendly Interface
        * Supports compliance reporting for various standards (e.g., PCI-DSS, HIPAA).
    * Cons
        * Subscription based model can be expensive and additional costs for advanced features and modules
        * Limited customization in creating custom scans compared to tools like Nmap
* Rapid7 Nexpose
    * Nexpose is a powerful vulnerability scanner from Rapid7 that helps you identify, prioritize, and remediate vulnerabilities.
    * Usage:
        * Dynamic asset discovery
        * Vulnerability assessment
        * Risk prioritization
        * Can also be integrated with Metasploit for exploit verification
    * Pros:
        * Comprehensive vulnerability coverage.
        * Integration with Metasploit.
        * Detailed remediation guidance.
    * Cons:
        * Requires a subscription.
        * Can be resource-intensive.
