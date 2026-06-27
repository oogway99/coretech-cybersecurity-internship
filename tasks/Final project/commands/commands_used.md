#	Attacker’s info:
commands used (hostname, hostname –I, cat /etc/os-release)
# Target info (metasploitable 2)
commands used (hostname, ifconfig, uname -a)
# Reconnaissance
a)	Network Connectivity Verification

Commands used: ping 150.1.7.102

b)	Host Discovery

Commands used: netdiscover -r 150.1.7.1

c)	ARP Cache Inspection

Commands used: arp –a

d)	Initial Port Scanning of metasploitable

Commands used: nmap -sS 150.1.7.102, nmap -sV 150.1.7.102, nmap -A 150.1.7.102
#	Enumeration
a)	FTP Enumeration (Port 21)

commands used: ftp 150.1.7.102

b)	SMB Enumeration (Port 139/445)

Command use: enum4linux -a 150.1.7.102

c)	HTTP Enumeration (Port 80)

Commands used: http://150.1.7.102 (for preview of webpage)

Command used: nikto –h http://150.1.7.102

d)	Telnet Enumeration (Port 80)

Command used telnet 150.1.7.102
# Post-Enumeration
a)	Run an Nmap Vulnerability Scan

Command used: nmap --script vuln 150.1.7.102

b) Web Server Assessment

Command used: nikto –h http://150.1.7.102

c)	Search for Public Exploits

Command used: searchsploit <service_name>

