<h1>Nmap Port Scanning</h1>


<h2>Description</h2>
This project focuses on network enumeration using Nmap to identify live hosts on a vulnerable system. Port scanning is a critical step in the reconnaissance phase of penetration testing, enabling security professionals to gather essential information about target systems before moving to the exploitation stage.
<br />


<h2>Tools Used</h2>

- <b>Nmap</b> 

<h2>Environments Used </h2>

- <b>Kali Linux</b>

<h2>Enumeration walk-through:</h2>

<p align="center">
Launch the attacking VM: <br/>
<img src="https://github.com/Kieyontay/NmapLab/blob/main/Kali%20System%20Startup.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Launch the target VM:  <br/>
<img src="https://github.com/Kieyontay/NmapLab/blob/main/Metasploitable%202%20Startup.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run Nmap 192.168.69.2: <br/>
<img src="https://github.com/Kieyontay/NmapLab/blob/main/Nmap%20basic%20port%20scan.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br />
Nmap command will run a basic port scan against the target machine showing which ports are open and the services running on them. For example, port 22 is showing as open and has SSH as the service which means a remote service is running, allowing for a potential brute-force attack if there are weak credentials present in the system.<br />
<br />
Run Nmap -sV -n 192.168.69.2:  <br/>
<img src="https://github.com/Kieyontay/NmapLab/blob/main/Nmap%20service%20port%20scan.png?raw=true" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br />
-sV enables us to identify what services and their versions are running on the target machine which will enable us to identify any vulnerabilities such as outdated versions that can be exploited.<br />
<br />
-n disables reverse-dns lookup, preventing Nmap from resolving IP addresses to hostnames, improving scan efficiency. 
<br />
<br />
At this stage of the reconnaisance phase, we are able use Nmap to identify potentially vulnerable services running on our target machine and gather information that can be used to assess potential vulnerabilities and attack vectors. We can use publicly available vulnerability databases to research service versions and identify any associated known vulnerabilities, helping to assess whether they may be exploitable in a given environment.
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
