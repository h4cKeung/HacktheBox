```bash
[*] ssh on tcp/22

	[-] Bruteforce logins:

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 22 -o "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp22/tcp_22_ssh_hydra.txt" ssh://10.10.11.166

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 22 -O "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp22/tcp_22_ssh_medusa.txt" -M ssh -h 10.10.11.166

[*] smtp on tcp/25

	[-] Try User Enumeration using "RCPT TO". Replace <TARGET-DOMAIN> with the target's domain name:

		hydra smtp-enum://10.10.11.166:25/rcpt -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -o "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp25/tcp_25_smtp_user-enum_hydra_rcpt.txt" -p <TARGET-DOMAIN>

[*] domain on tcp/53

	[-] Use dnsrecon to bruteforce subdomains of a DNS domain.

		dnsrecon -n 10.10.11.166 -d <DOMAIN-NAME> -D /usr/share/seclists/Discovery/DNS/subdomains-top1million-110000.txt -t brt 2>&1 | tee /home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/tcp_53_dnsrecon_subdomain_bruteforce.txt

	[-] Use dnsrecon to automatically query data from the DNS server. You must specify the target domain name.

		dnsrecon -n 10.10.11.166 -d <DOMAIN-NAME> 2>&1 | tee /home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp53/tcp_53_dnsrecon_default_manual.txt

[*] http on tcp/80

	[-] (gobuster v3) Multi-threaded directory/file enumeration for web servers using various wordlists:

		gobuster dir -u http://10.10.11.166:80/ -t 250 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -e -k -x "txt,html,php,asp,aspx,jsp" -o "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_gobuster_dirbuster.txt"

	[-] Credential bruteforcing commands (don't run these without modifying them):

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 80 -o "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_auth_hydra.txt" http-get://10.10.11.166/path/to/auth/area

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 80 -O "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_auth_medusa.txt" -M http -h 10.10.11.166 -m DIR:/path/to/auth/area

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 80 -o "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_form_hydra.txt" http-post-form://10.10.11.166/path/to/login.php:"username=^USER^&password=^PASS^":"invalid-login-message"

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 80 -O "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_form_medusa.txt" -M web-form -h 10.10.11.166 -m FORM:/path/to/login.php -m FORM-DATA:"post?username=&password=" -m DENY-SIGNAL:"invalid login message"

	[-] (nikto) old but generally reliable web server enumeration tool:

		nikto -ask=no -h http://10.10.11.166:80 2>&1 | tee "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_nikto.txt"

	[-] (wpscan) WordPress Security Scanner (useful if WordPress is found):

		wpscan --url http://10.10.11.166:80/ --no-update -e vp,vt,tt,cb,dbe,u,m --plugins-detection aggressive --plugins-version-detection aggressive -f cli-no-color 2>&1 | tee "/home/kali/Desktop/HTB/HacktheBox/Machines/10.10.11.166-trick/results/10.10.11.166/scans/tcp80/tcp_80_http_wpscan.txt"


```