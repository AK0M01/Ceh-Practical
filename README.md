# CEH PRACTICAL
Q1 FQDN
* nmap -p389 -sV <subnet> -Pn
*          OR
* nmap -A <subnet> -Pn

Q2 Wamp Server
* nmap -A -sV -p 80,8080,443

Q3 SMB 
* nmap -p 445 <subnet>
* hydra -l Henry -P <password.txt file on desktop> <ip> smb
* smbclient
