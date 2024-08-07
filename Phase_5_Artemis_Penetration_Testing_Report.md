# Cybersecurity-Capstone-Project Phase 5


Artemis Penetration Testing Report \


 \
May 14, 2024 \
 \
By: Eseosa Igiozee

Table of Contents

Contents……………………………………………………………………………………........1 

1.0 Executive Summary……………………………………………………………………….........3 \
1.1 Scope of Work……………………………………………………………………………...5

1.2 Project Objectives…………………………………………………………………………..5 \
1.3 Assumption………………………………………………………………………………….6

1.4 Timeline………………………………………………………………………………………6  \
1.5 Summary of Findings……………………………………………………………………….6

1.6 Recommendations……………………………………………………………12 \


1.0 Executive Summary

Artemis Gas, Inc., an established company in the industrial gas sector, is confronted with substantial cybersecurity threats that have the potential to jeopardize its operational reliability and competitive position. This report identifies crucial vulnerabilities within our IT infrastructure and assesses the corresponding risks to our company operations. The customer is concerned about the vulnerabilities in Artemis' web application, particularly the lack of restrictions or filtering on user uploads based on file type. In our assessment of the Artemis web application, we will also be evaluating the Artemis internet infrastructure and identifying any other vulnerabilities that may exist. 


<table>
  <tr>
   <td><strong>Severity</strong>
   </td>
   <td><strong>CVSS V2 Score Range</strong>
   </td>
   <td><strong>Definition</strong>
   </td>
  </tr>
  <tr>
   <td><strong>High</strong>
   </td>
   <td>7.0 - 10.0
   </td>
   <td>Exploitation is simple and almost always ends in system compromise. It is recommended to fix the bug as soon as possible.
   </td>
  </tr>
  <tr>
   <td><strong>Medium</strong>
   </td>
   <td>4.0 - 6.9
   </td>
   <td>These sets of Vulnerabilities aren't exploitable. After fixing vulnerabilities with high severity, plan to patch up next.
   </td>
  </tr>
  <tr>
   <td><strong>Low</strong>
   </td>
   <td>0.0 - 3.9
   </td>
   <td>Vulnerabilities aren't exploitable, yet they can help a company's attack surface. It is recommended to plan and patch the software bug.
   </td>
  </tr>
  <tr>
   <td><strong>Information</strong>
   </td>
   <td>N/A
   </td>
   <td>There isn't any vulnerability. Further information on things discovered during testing.
   </td>
  </tr>
</table>


To guarantee the confidentiality, integrity, and availability of data, it is imperative that Artemis Gas, Inc promptly addresses these vulnerabilities. These vulnerabilities can be easily discovered through basic reconnaissance and can be exploited without much effort, as stated in the security assessment findings.  It should be noted that this assessment may not uncover all vulnerabilities that exist on the systems included in the scope. Any modifications made to the environment during the testing phase may impact the outcomes of the assessment.


## Business Impact Classifications


<table>
  <tr>
   <td><strong>Impact</strong>
   </td>
   <td><strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Major</strong>
   </td>
   <td>Successful exploitation may result in large disruptions of critical business functions across the organization and significant financial damage.
   </td>
  </tr>
  <tr>
   <td><strong>Moderate</strong>
   </td>
   <td>Successful exploitation may cause significant disruptions to non-critical business functions.
   </td>
  </tr>
  <tr>
   <td><strong>Minor</strong>
   </td>
   <td>Successful exploitation may affect few users, without causing much disruption to routine business functions.
   </td>
  </tr>
</table>



## Technical Report

Apollo Security performed an external penetration test on Artemis Gas Inc's network in May 2024. The Apollo Security team performed External Box penetration testing on the Artemis Web Application server with the objective of gaining access to the Artemis business network infrastructure.

The objective of this assessment was to identify vulnerabilities in Artemis Gas Inc's infrastructure and provide recommendations for their resolution. During the duration of the engagement, Apollo Security detected high-level vulnerabilities that allowed unrestricted access to the internal network. These vulnerabilities are categorized by severity and presented in the table below.

**1.1. Scope of Work**

This report provides an in-depth review of the results obtained from doing a comprehensive vulnerability assessment and threat analysis for Artemis Gas, Inc. The scope includes evaluations of network, web application client, and the IT Client Environment, covering critical infrastructure and applications.

**1.2 Project Objectives**

The objective of this assessment is to uncover and document the vulnerabilities and weaknesses in Artemis's internet infrastructure and web application. We will conduct tests on items that pose significant vulnerability concerns and also provide them CVSS scores to identify those that require immediate assessment and remediation.

**1.3 Assumptions**

The assumptions that we are making while writing this report is that the IP addresses are all to be considered public information and that we have been granted full access to Artemis’ network and systems in order to obtain an accurate assessment of the IT Client Environment and Web Application. 

**1.4 Timeline**

The timeline of the test is as below:


<table>
  <tr>
   <td>Penetration Testing
   </td>
   <td>Start Date 
   </td>
   <td>End Date
   </td>
  </tr>
  <tr>
   <td>Phase 1: Perform Reconnaissance 
   </td>
   <td>05/05/2024
   </td>
   <td>05/06/2024
   </td>
  </tr>
  <tr>
   <td>Phase 2: Identify Targets and Run Scans
   </td>
   <td>05/06/2024
   </td>
   <td>05/08/2024
   </td>
  </tr>
  <tr>
   <td>Phase 3: Identify Vulnerabilities
   </td>
   <td>05/08/2024
   </td>
   <td>05/09/2024
   </td>
  </tr>
  <tr>
   <td>Phase 4: Threat Assessment
   </td>
   <td>05/09/2024
   </td>
   <td>05/11/2024
   </td>
  </tr>
  <tr>
   <td>Phase 5: Reporting
   </td>
   <td>05/12/2024
   </td>
   <td>05/14/2024
   </td>
  </tr>
</table>


**1.5 Summary of Findings**

During the assessment, we identified 9 scenarios that require review. Among these reviews, the following tables and CVSS score findings are presented. 

The Risk Matrix below is utilized to understand the likelihood and severity of an attack:


![Capture](https://github.com/user-attachments/assets/76efaac7-18e7-4a0a-af37-33fa7331fd48)


<table>
  <tr>
   <td><strong>Scenario #</strong>
   </td>
   <td><strong>CVSS Score</strong>
   </td>
   <td><strong>Severity</strong>
   </td>
  </tr>
  <tr>
   <td>1
   </td>
   <td>9.8
   </td>
   <td>Critical
   </td>
  </tr>
  <tr>
   <td>2
   </td>
   <td>9.0
   </td>
   <td>Critical
   </td>
  </tr>
  <tr>
   <td>3
   </td>
   <td>10.0
   </td>
   <td>Critical
   </td>
  </tr>
  <tr>
   <td>4
   </td>
   <td>7.8
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>5
   </td>
   <td>7.5
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>6
   </td>
   <td>7.0
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>7
   </td>
   <td>9.8
   </td>
   <td>Critical
   </td>
  </tr>
  <tr>
   <td>8
   </td>
   <td>8.0
   </td>
   <td>High
   </td>
  </tr>
  <tr>
   <td>9
   </td>
   <td>9.1
   </td>
   <td>Critical
   </td>
  </tr>
</table>


Artemis has significant vulnerabilities in their information security, as identified during our penetration tests. At the moment, we have  5 critical vulnerabilities and 4 high vulnerabilities. It is imperative to promptly resolve the critical vulnerabilities and follow the suggestions outlined in our recommendation section 1.6.

It is crucial to invest in examining the CIS Control v8 Benchmarks and creating security policies based on the standard recommendations of at least level 1 controls. This upgrade is necessary and should be done immediately. The following are the results of the scenarios.

**Scenario 1: Unpatched RDP is exposed to the internet**

In the first scenario, we will examine the Unpatched RDP (Remote Desktop Protocol) that is exposed to the internet. When evaluating the threats of this situation, it is crucial to understand the level of risk it poses. In this scenario, enabling internet accessibility for the RDP permits individuals to remotely access the system even if they are not affiliated with the company. If an attacker gains access to an admin account, they have the potential to inflict serious damage to the systems, databases, and web application. RDP has been affected by numerous vulnerabilities, including TeamViewer, VNC, and Bluekeep, which have a documented history of causing significant damage.

**Scenario 2: Web application is vulnerable to SQL Injection**

SQL Injections are a type of attack that occurs when the attacker executes malicious SQL statements. An SQL Injection poses the risk of allowing the attacker to bypass the security of the web application by using SQL statements. This particular sort of attack has consistently ranked among the top 10 vulnerabilities on the OWASP list for an extended period of time, making it a highly common and widespread attack. Risks include unauthorized access to the entire SQL database and the ability for the attacker to modify information within the web application. Unauthorized access to the database might potentially expose highly sensitive information, including client data, personal information, intellectual property, and even confidential trade secrets. 

**Scenario 3: Default password on Cisco admin portal**

A common problem that arises is the failure to modify the default password for admin information during the first configuration and setup of network information. Upon investigation, we discovered that the Cisco admin interface is still using the default password. For instance, a simple online search revealed that the default password for Cisco settings is "cisco". Armed with such information, someone with malicious motives could inflict substantial harm upon your organization with minimal exertion. After successfully logging into the Cisco admin portal, the person has the ability to easily change the password and prevent you from accessing the portal. This could lead to unauthorized access to the data and devices connected to the network through web applications.

**Scenario 4: Apache web server vulnerable to CVE-2019-0211**

This vulnerability is very specific to Apache. In 2019, a vulnerability was discovered that allowed an attacker to run unprivileged scripts, leading to a complete takeover of the main Apache process. This poses a security risk as it grants someone root privileges, enabling them to get access to shared environments and databases. The potential risk in this situation can be significant, depending on the nature of the supplied information. Even if the web server is not actively functioning, there is still a possibility of a series of additional attacks that could result in a data breach. 

**Scenario 5: Web server is exposing sensitive data**

When referring to a web server revealing sensitive data, it typically implies the publication of personally identifiable information. This may include sensitive data such as social security numbers, financial information, and even login credentials. This data exposure commonly occurs as a result of insufficient safeguards for a database, improper utilization of data systems, and misconfigurations during the implementation of new datastores in new instances. The consequences of this might vary from financial penalties imposed by regulatory authorities such as HIPAA and HITECH, to problems with public image and the reputation of the company. These types of exposures can occur through various means, including SQL Injections, Bad Access Control, Ransomware, and Network Compromise. 

**Scenario 6: Web application has broken access control**

Broken access control for a web application means that the web application itself is not properly managing who and what has access to the web application. These occurrences can arise from either injection vulnerabilities, cross-site scripting, or improper authentication and session management. The vulnerability clearly poses a significant danger of a data breach and unauthorized access to information. Similar to other weaknesses, this can result in non-compliance with regulatory standards, substantial periods of downtime and disruptions to operations. 

**Scenario 7: Oracle WebLogic Server vulnerable to CVE-2020-14882**

CVE-2020-14882 is a remote code execution flaw in the Oracle WebLogic Server. This exploit has a low level of complexity and is considered to be easily exploitable. The vulnerability was assigned a CVSS score of 9.8, indicating its critical severity, and it enables full control over the host.  To prevent this issue, it is recommended to update Oracle WebLogic Server to its latest version and enable the application patches. 

**Scenario 8: Misconfigured cloud storage (AWS security group**

**misconfiguration, lack of access restrictions)**

Misconfigured cloud storage can be vulnerable to many risks, including unrestricted inbound/outbound ports, insecure automated backups, and deactivated monitoring and logging. Poor port management and inadequate backups can result in a system compromise of data, rendering crucial data inaccessible after a catastrophic incident or making it very vulnerable due to weak security measures.

**Scenario 9: Microsoft Exchange Server vulnerable to CVE-2021-26855**

This vulnerability was detected and exploited as a zero-day attack for over two months before it was identified and addressed. The Exploit, identified in 2021, utilizes the Microsoft Exchange Server to exploit HTTPS communications, enabling unauthorized user access authentication. During the occurrence of this vulnerability, it was assigned a CVSS score of 9.1, categorizing it as Critical. 

**1.6 Summary of Recommendation**

These are the recommendations for the following scenarios in order to try and resolve these. 

**Scenario 1: Unpatched RDP is exposed to the internet**

Possible consequences include being denied access to vital information, data loss, and public relations problems arising from compromised client or customer information. One effective way to prevent or detect this issue is by implementing a Remote Desktop Protocol (RDP) Log Audit to check the credentials of people accessing the system. Additionally, implementing requirements for accessing the RDP by requiring a specific VPN connection. Furthermore, minimizing the vulnerability to external threats by completely shutting down RDP ports and permitting RDP access solely within the intranet.

**Scenario 2: Web application is vulnerable to SQL Injection**

The consequences of an event like this could include a significant disruption to business operations, damage to public perception, and financial penalties imposed by regulatory authorities. There is also the possibility of falling victim to ransomware, a situation in which individuals are denied access to their data and compelled to pay a ransom in order to regain access. To prevent this issue, it is advisable to do SQL penetration testing to identify vulnerabilities in your system and subsequently address them. Many open source tools and SIEM programs have the ability to identify and highlight weaknesses in a system.

**Scenario 3: Default password on Cisco admin portal**

It is important to quickly modify the password of your admin portals as soon as they are established in order to address this issue effectively. This item should be included in your policies and procedures and should be subject to monthly audits to ensure that no mistakes go overlooked. 

**Scenario 4: Apache web server vulnerable to CVE-2019-0211**

To fix this situation, it is necessary to ensure that Apache is updated to version 2.4.39 or a more recent release. In order to better address these types of problems, it is crucial to establish a monthly auditing system for all software to ensure that we are applying software updates more often. Apache is a highly popular open source program. It is advisable to closely monitor bulletin boards that provide information about potential vulnerabilities in the future. This vulnerability has minimal exploitability yet a significant impact.

**Scenario 5: Web server is exposing sensitive data**

To mitigate this risk effectively, it is crucial to establish robust security measures, categorize and maintain data, encrypt all sensitive data at rest, and regularly assess potential data-related threats. By implementing the NIST controls, you can effectively establish systems, conduct audits, and maintain logging procedures to prevent the unauthorized exposure of sensitive data.  

**Scenario 6: Web application has broken access control**

The best way to prevent broken access control is to set up access validation. If unauthorized individuals are trying to get entry to the database without appropriate authorization, their attempts will be denied. Effective management of the access control and frequent audits of the access control can mitigate these types of problems. Referring back to the NIST Benchmarks and Controls will work effectively to mitigate the risk by reviewing access logs.

**Scenario 7: Oracle WebLogic Server vulnerable to CVE-2020-14882**

The way to prevent this is to update Oracle WebLogic Server to its most recent version and allow it to be patched out. Similar to other situations, it is crucial to establish suitable measures to address vulnerabilities in software patches and establish regular schedules for updates in order to protect internal information.

**Scenario 8: Misconfigured cloud storage (AWS security group**

**misconfiguration, lack of access restrictions)**

The consequences of this can lead to disruption of business in the event of failing to back up your databases appropriately, all the way to your database being maliciously encrypted and falling victim to ransomware. To prevent this occurrence, it is crucial to effectively organize your data, establish strong security policies and templates, and regularly audit cloud configurations to stay informed about any alterations or vulnerabilities. 

**Scenario 9: Microsoft Exchange Server vulnerable to CVE-2021-26855**

The risk associated with this attack is the entire penetration of your authentication servers, which would allow anyone utilizing the Microsoft Exchange Servers vulnerable to this exploit. Consequently, it would grant the intruder unrestricted access to all data being utilized by the affected user. To mitigate this occurrence, it is important to regularly update your software and closely monitor any potential vulnerabilities that could affect your business. First, prioritize the maintenance of any servers that are accessible from outside the network, and then proceed to address internal servers in order to minimize any potential disruptions. 
