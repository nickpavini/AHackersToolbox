# AHackersToolbox
A list of Penetration Testing (Hacking) tools that can be used, as well as some helpful information and examples. For educational purposes only.

**Note**: No download procedures means it comes with kali linux.

![Monty Python](intruder.png) ![Monty Python](intruder.png)

Nmap
----
Network scanning tool: Use this to identify open ports, running services and other information about the server.

```
nmap -v -A 1.2.3.4
```


DIRB
----
Web scanner. Use this to find file paths, directories, etc; of content on a webapp

```
dirb -w http://1.2.3.4
```


Enum4Linux
----------

```
```


Aircrack-ng
-----------
Brute force WiFi password cracking.

```
```


HashID
------
Use this to assist in determining what type of hash is being dealt with. The output of this can help you determine settings needed in hashcat or johntheripper

```
hashid -m -j hash.txt
```


SSH2John
--------
Strip an ssh2 format private key file of its encryption hash for cracking with JohnTheRipper.

Note: Private key files (ex. id_rsa) can be password protected to help secure them in case they are lost/stolen, ssh2john retrieves the hashed password.

**Download and Run**
```
wget https://raw.githubusercontent.com/magnumripper/JohnTheRipper/bleeding-jumbo/run/ssh2john.py
python ssh2john.py id_rsa > id_rsa.hash
```


JohnTheRipper
-------------
Brute force password cracking of hashed passwords

```
john --wordlist=/path/to/wordlist.txt --format=format hash.txt
```


HashCat
-------
Bruce force password cracking of hashes

```
hashcat -m 3200 hash.txt /path/to/wordlist
```


LinEnum
-------
Use this to assist in locating potential methods of privelege escalation on linux.

**Download, make executable, and run**
```
wget https://raw.githubusercontent.com/rebootuser/LinEnum/master/LinEnum.sh
chmod +x LinEnum.sh
./LinEnum.sh -s -r report -t
```


Hydra
-----
Network brute force login cracker

```
hydra -l Elliot -P fsocity.dic 10.10.103.0 -V http-form-post '/wp-login.php:log=^USER^&pwd=^PASS^&wp-submit=Log+In&redirect_to=http%3A%2F%2F10.10.103.0%2Fwp-admin%2F&testcookie=1:F=is incorrect'
```
