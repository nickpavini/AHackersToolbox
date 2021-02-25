# AHackersToolbox
A list of Penetration Testing (Hacking) tools that can be used, as well as some helpful information and examples. For educational purposes only.

**Note**: No download procedures means it comes with kali linux.



Nmap
----
Network scanning tool: Use this to identify open ports, running services and other information about the server.

```
nmap -v -A 1.2.3.4
```


DIRB
----

```
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
```


LinEnum
-------
Use this to assist in locating potential methods of privelege escalation on linux.

```
```

