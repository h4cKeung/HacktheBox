```bash
nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 53 --script="banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/tcp_53_dns_nmap.txt" -oX "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/xml/tcp_53_dns_nmap.xml" 10.10.11.166
```

[/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/tcp_53_dns_nmap.txt](file:///home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/tcp_53_dns_nmap.txt):

```
# Nmap 7.92 scan initiated Sat Aug 13 07:23:26 2022 as: nmap -vv --reason -Pn -T4 --min-rate=1000 -sV -p 53 "--script=banner,(dns* or ssl*) and not (brute or broadcast or dos or external or fuzzer)" -oN /home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/tcp_53_dns_nmap.txt -oX /home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/xml/tcp_53_dns_nmap.xml 10.10.11.166
Nmap scan report for 10.10.11.166
Host is up, received user-set (0.095s latency).
Scanned at 2022-08-13 07:23:29 EDT for 23s

PORT   STATE SERVICE REASON  VERSION
53/tcp open  domain  syn-ack ISC BIND 9.11.5-P4-5.1+deb10u7 (Debian Linux)
|_dns-nsec-enum: Can't determine domain for host 10.10.11.166; use dns-nsec-enum.domains script arg.
|_dns-nsec3-enum: Can't determine domain for host 10.10.11.166; use dns-nsec3-enum.domains script arg.
| dns-nsid: 
|_  bind.version: 9.11.5-P4-5.1+deb10u7-Debian
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Host script results:
|_dns-brute: Can't guess domain of "10.10.11.166"; use dns-brute.domain script argument.

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 13 07:23:52 2022 -- 1 IP address (1 host up) scanned in 26.39 seconds

```
