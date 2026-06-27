# Findings
The vulnerability assessment and penetration testing exercise identified multiple security weaknesses on the Metasploitable 2 target system. Network reconnaissance revealed numerous open ports exposing services such as FTP, Telnet, HTTP, SMB, SSH, SMTP, and database services. Service enumeration confirmed that several applications were outdated and matched publicly documented vulnerabilities. 
Anonymous FTP access was enabled, allowing unauthenticated users to access the FTP service. SMB enumeration disclosed user accounts, shared resources, and operating system information, providing valuable intelligence for potential attackers. The Telnet service accepted remote connections, transmitting authentication data without encryption and increasing the risk of credential compromise. Web server assessment using Nikto identified outdated Apache components, insecure HTTP configurations, and other web server misconfigurations.
Vulnerability scanning and public exploit research confirmed that several detected services had known exploits available in public exploit databases. Controlled exploitation within the isolated laboratory environment successfully demonstrated that vulnerable services could be compromised, validating the identified security weaknesses. Post-exploitation activities further confirmed the ability to gather system information and assess the potential impact of a successful attack.
Overall, the assessment demonstrated that the target system contains intentionally vulnerable configurations suitable for security training. In a production environment, these weaknesses would present a significant risk to the 
confidentiality, integrity, and availability of organizational assets.

# risk analysis

Findings|Severity|Potential|Impact|Risk Level
Anonymous|Ftp Access|Medium|Unauthorized|File Access|Medium
Telnet Service Enabled|High|Credential Interception|High
Outdated Apache Web Server|High|RemoteExploitation|High
Smb Information Disclosure|High|User And SystemEnumeration|High
Publicly Available Service Exploits|Critical|Remote Code Execution|Critical
Multiple Open Network Services|Medium|Increased Attack Surface|Medium

