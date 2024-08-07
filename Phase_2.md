Eseosa Igiozee

In phase 1, the goal was to build as robust a profile on the target, Artemis as possible. The deliverable covered 15 tools and methods that would be used to accomplish this task of reconnaissance. For phase 2, the goal is to now identify the tools and techniques to be used to perform host discovery and enumeration. Listed below will be the tools that will be used to perform network scans, the purpose for using them, and how it will be used. 



1. Nmap
    * Nmap (Network Mapper) is a versatile network scanning tool that is known for being able to quickly discover hosts, services, and their configurations. It supports a variety of scan types, including TCP SYN, ping, and version detection, making it ideal for detecting open ports, identifying services, and comprehending network architecture.
    * Usages: 
        * Host discovery
            * Nmap can identify live hosts within the Artemis network by doing a simple ping sweep.
            * Command: nmap -sn ###.###.#.#**/**##
        * Port scanning
            * A SYN scan will reveal any open ports and associated services (such as SSH, HTTP, or RDP).
            * Command: nmap -sS  ###.###.#.###
        * Service and version detection
            * Nmap's version detection capability provides detailed information about software versions running on open ports.
            * Command: nmap -sV ###.###.#.###
        * OS detection
            * Fingerprinting can help determine the operating system of a device.
            * Command: nmap -O ###.###.#.###
        * Vulnerability scanner
            * Nmap can find vulnerabilities in the network through the Nmap Script Engine (NSE) – a flexible feature activated with the -sC option that allows users to write scripts for task automation.
            * Command: nmap --script=vuln ###.###.#.###
2. OpenVAS
    * OpenVAS (Open Vulnerability Assessment System) is a free and open-source vulnerability scanner made to find possible security holes in various network services. It uses a database of known vulnerabilities to provide detailed information about misconfigurations, outdated software, and exploitable flaws.
    * Usages:
        * Vulnerability Scanning
            *  Perform a comprehensive scan of Artemis’ external IP addresses to identify unpatched software or insecure configurations.
        * Reporting
            *  Use OpenVAS's reporting feature to organize and analyze findings, presenting vulnerabilities by severity to prioritize remediation efforts.
3. Nikto
    * Nikto is a web server vulnerability scanner that detects potentially harmful files, outdated software versions, and insecure HTTP parameters. It is very successful in assessing web servers for a variety of common issues, revealing previously unnoticed misconfigurations.
    * Usages:
        * Basic Scanning:
            *  Run a basic scan against Artemis' web applications to identify outdated software or risky configurations like directory listing.
        * Custom Scans:
            *  Focus scans on specific vulnerabilities, such as exposed admin panels or unnecessary services.
4. Wireshark
    * Wireshark is a packet analysis tool that captures and analyzes network traffic. It provides detailed insights into data exchanges, highlighting communication protocols and potential vulnerabilities in data transmission.
    * Usages:
        * Traffic Monitoring:
            *  Capture network traffic in segments where sensitive data is exchanged to analyze communication patterns.
        * Protocol Analysis:
            *  Identify protocols in use and assess their security (e.g., HTTP vs. HTTPS, FTP vs. SFTP).
        * Troubleshooting:
            *  Detect anomalies or possible data leaks that could be indicative of security misconfigurations.
5. Metasploit
    * Metasploit is a comprehensive framework that helps penetration testers in identifying and exploiting vulnerabilities. It has built-in modules for reconnaissance, scanning, and exploitation, which simplifies the process of testing for weaknesses in identified services.
    * Usages:
        * Service Detection:
            *  Use the auxiliary modules to perform scans and detect active services.
        * Exploit Testing:
            *  Test identified vulnerabilities (e.g., outdated software) by safely running exploits from Metasploit’s library.
        * Payload Generation:
            *  Craft payloads to simulate post-exploitation attacks and understand the full impact of security flaws.
    * Commands: 
        * Use “sudo msfconsole” to start metasploit
        * To do service detection use “ set RHOSTS TARGET_IP “ 
            * Change target_IP to the IP address that is being targeted
        * To do exploit testing after using RHOSTS target_ip, use set payload cmd/unix/interact and then use exploit
