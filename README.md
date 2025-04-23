# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find out the ip address of the attackers system
## OUTPUT:
# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

Find out the ip address of the attackers system
## OUTPUT:


![Screenshot 2025-03-27 101111](https://github.com/user-attachments/assets/5b0fea40-1ec6-46d4-8ebc-4ed3546a7c54)

Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows:

systemctl start postgresql

msfdb init

Invoke msfconsole:
## OUTPUT:
![5 2n n](https://github.com/user-attachments/assets/a1f724ba-bc8f-4ea8-980f-410d16c3d5c5)


Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![5 3nn](https://github.com/user-attachments/assets/bb08085f-09a7-4619-8573-cfdd2feceb3f)

Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
## Output:
![5 4nn](https://github.com/user-attachments/assets/783fc97a-b0ff-4b5d-8f11-5499f83b9186)

step4: use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24
## output:
![image](https://github.com/user-attachments/assets/81eb6a97-05e3-428f-9a25-b1b5f2a4c31c)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
## output:

![image](https://github.com/user-attachments/assets/78d0b1a5-c452-4c76-aa85-82d0b879e258)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit

![5 7n](https://github.com/user-attachments/assets/e428e346-7c96-4735-9813-463e5c80635f)

The info command provides information regarding a module or platform,


![Screenshot 2025-03-29 135513](https://github.com/user-attachments/assets/889ca7ab-1545-43ea-b8ae-5fcf31fb04d1)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows:

systemctl start postgresql

msfdb init
## MYSQL ENUMERATION
Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>

![Screenshot 2025-03-29 135553](https://github.com/user-attachments/assets/a57bb53c-9834-4bbd-8901-40cee27a069f)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql

![Screenshot 2025-03-29 135643](https://github.com/user-attachments/assets/8be25a44-fb5d-43a4-b84b-5695e60dc507)
use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version


![Screenshot 2025-03-29 141955](https://github.com/user-attachments/assets/aea21e20-e746-43aa-9e52-ccc5ae294a4b)
Use the set rhosts command to set the parameter and run the module, as follows:


![Screenshot 2025-03-29 135857](https://github.com/user-attachments/assets/e290776a-b601-47ce-89c7-a78285a53197)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

![Screenshot 2025-03-29 140320](https://github.com/user-attachments/assets/150b91f6-6bd8-4d3c-9d20-900305a1f513)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists:

set PASS_FILE /usr/share/wordlists/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS

Set BLANK_PASSWORDS to true in case there is no password set for the root account.

set BLANK_PASSWORDS true
![Screenshot 2025-03-29 140558](https://github.com/user-attachments/assets/0e53633f-bf22-4d6a-b3b0-efc1e66dcf2f)


## RESULT:
The Metasploit framework for reconnaissance is  examined successfully


Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows:

systemctl start postgresql

msfdb init

Invoke msfconsole:
## OUTPUT:


![Screenshot 2025-03-27 101159](https://github.com/user-attachments/assets/4fdca92d-8382-41ad-bdf4-6e33193eae88)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.


![Screenshot 2025-03-27 101225](https://github.com/user-attachments/assets/73734f31-89b1-453d-b5fd-6572138eacdc)
Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
## Output:

![Screenshot 2025-03-29 131753](https://github.com/user-attachments/assets/57b5052e-4e8f-431f-83c2-0fc41b49cd8c)
step4: use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24
## output:

![5](https://github.com/user-attachments/assets/cb727cf7-cf24-4e61-a0f6-8c68b8ec244e)
Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l
## output:


![Screenshot 2025-03-29 132004](https://github.com/user-attachments/assets/1927b7c6-c5e4-4aee-8cfa-68518cf197af)
Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit


![Screenshot 2025-03-29 135422](https://github.com/user-attachments/assets/72c24381-213a-4e44-bda8-9edafe3f3634)
The info command provides information regarding a module or platform,


![Screenshot 2025-03-29 135513](https://github.com/user-attachments/assets/889ca7ab-1545-43ea-b8ae-5fcf31fb04d1)
Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows:

systemctl start postgresql

msfdb init
## MYSQL ENUMERATION
Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>

![Screenshot 2025-03-29 135553](https://github.com/user-attachments/assets/a57bb53c-9834-4bbd-8901-40cee27a069f)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql

![Screenshot 2025-03-29 135643](https://github.com/user-attachments/assets/8be25a44-fb5d-43a4-b84b-5695e60dc507)
use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version


![Screenshot 2025-03-29 141955](https://github.com/user-attachments/assets/aea21e20-e746-43aa-9e52-ccc5ae294a4b)
Use the set rhosts command to set the parameter and run the module, as follows:


![Screenshot 2025-03-29 135857](https://github.com/user-attachments/assets/e290776a-b601-47ce-89c7-a78285a53197)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

![Screenshot 2025-03-29 140320](https://github.com/user-attachments/assets/150b91f6-6bd8-4d3c-9d20-900305a1f513)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists:

set PASS_FILE /usr/share/wordlists/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS

Set BLANK_PASSWORDS to true in case there is no password set for the root account.

set BLANK_PASSWORDS true
![Screenshot 2025-03-29 140558](https://github.com/user-attachments/assets/0e53633f-bf22-4d6a-b3b0-efc1e66dcf2f)


## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
