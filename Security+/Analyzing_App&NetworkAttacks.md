# Privledge Escalation 
> Leverages programming errors and design flaws to get to elevated access to network and related systems, data and applications
> 
> * Can happen durring attack kill chain or penetration testing
> 
> * Higher privledges can lead to bigger damage
>
> * Can be vertical vs Horzizonatal

> Advance Persistent Threats attempt an escaltion of access privledges soon after inital compromise
> *  goal to become root / Domain admin group member
> * Higher level == more access and more potential of damage
> * least privledge principles are key

> ### Process
> 1. Check OS of system
> 2. View kernel version
> 3. Check users and privedges
> 4. List the SUID files -- gives user who runs a file, run ass as owner
> 5. Check outdated software installs

# Cross-site Scripting and Request Forgery (XSS)

* Flaws in pages/webservers -- not necessarily in Apache/IIS
* malicious code inhected into trusted websites
* Malicious scripts can steal cookies, session tokens, etc
* can occur at anytime a web program uses user input within output it generates without validating or encoding

### Types of XSS attacks

* DOM based XSS (Local or Type 0)
    * Doesn't deal with servers
    * usually on vulnerable HTML
    *  Stock tickers, RSS clockk, Notifications etc

* Reflected XSS (Nonpersistent or Type 1)
    * Where the attcker provides script and user provides input
    * Most prevelent -- since not feasible to turn off scripting

* Stored XSS (Persistent or Type 2)
    * the script is loaded onto the server before serving to the victim

* Request Forgery (CSRF/XSRF)
    * Forces end user to perform undesirable actions in web app in which they are authenticated
    * Effective CSRF can force users to:
        * transfer $
        * change email
        * change password
    * Steps:
        1. Forge request
        2. Send to visitors
        3. Visitors click link and forgery sends funds to attacker

# Injection Attacks

* XSS and CSRF are two attacks agains HTTP and webservices and servers
* *Injection attack* often is a result of Man IN the Middle exploit or RAT (Remote access trojan) attack
* Malware can iject False MAC or IP addresses
* DLL Injection is where malicious code forces iteself to run within benign code
* Injected code is written by 3rd party developers  designed to perform a malicious function

## SQL Injection

* Allows for SQL query input data to be used for exploit
* Change dataabse
* Execute admin functions

## LDAP Injection

* Lightweight version of directory service
* Web Apps take input from client to process further -- attacker exploits when not properly handled
* Attacker can render sensistive user info or change info in LDAP directory

## XML Injection

* SOAP Injection
* User input inserted unsafely
* XML Metacharcters can modify XML stucture
* Can interfere app logic
    * Allows to perform unauthorized tasks or access data

# Targeted Coding Attacks

## Pointer Object Dereference

> Attacker suoplies pointer for mem location program doesnt expect
> 
> * Null pointers can be dereferences -- raises NullPointerException
> * Can allow for reading other mem locations
> * Null pointer errors are frequently the result of one or more programmer assumptions being violated

## Directory Traversal

> path traversal attack or "dot slash" often through web browsers or other clients
> 
> Allows attacket to access files, dirs, commands located outside of root directory
>
> * Attckrs can modify URI/URL to force web server to expse restricted files

## Buffer Overflow and IntegerOverflow

> Buffer
> * Attacker sends larger input and server accepts and writes to memeory areas
> * Associted buffers filles and memory overwritten
> * overwrite may contain instructs or crash server

> Integer
> * integer operation does not fit in mem space
> * causes Error in program

## Race Condition

> When system ro software tries to do two things simultaneously
> 
> Race conditions are related to synch errors
>
> crackers can leverage this to get unauthorized access

## Time of Check vs Time of Use attack

> When attacker gain privledges by "racing" to a resource it is attempting to acces
>
> Flaws here allow for race donitions when sys splits up ops of verifying creds and providing accessj
>
> Happens when sharing files, variables in multi-threaded operations
>
> Can replace a config.sys on windows to exploit an OS

## Improper Error and INput Handling

> Poorly defined validation rules used in verifying input
>
> SW Apps and servers are notorious
> 
> Must establish data input - flow - output reqs with sec features
> 
> COllisions are in this cat when the chance two unique inputs produce same result ie SHA-1 / MD5

## Session replay attack

> Attacker steals a calis session ID and resuses it
>
> IPSec and TLS have anti-replay mechanisms to protect the secure session


# API Attacks

> API DDoS often involves sending traffic from nay clients to overhwhlem API
>
> Rate limit to prevent server crashing cannot always prevent service distruption
>
> ## Vectors
>
> * Login Attacks
>
>   * Like Login Creds - API mamangement may not limit credential stuffing 
> * DDoS
> * MITM
> * Leveraging Credentials (Legit ones stolen through other exploits)

# SSL Stripping and Pass the Hash

## Pass the Hash
> Windows vulnerability
> * Crypto hashes within Windows can be recieved from various tools
> * Known as Pass the Hash
> *  Windows Virtual Service Module helps prevent it

> Windows Safe Mode is vulnerable
>
> It is OS dianostic module
>
> Can Only be run at Boot Time
>
> Most 3rd party sec products do now start in safe mode so protection negated

# Driver Manipulation

> Drivers in OS
>
> Privleged code trusted by OS
>
> Can be trojan, RAT or hacked driver software

## Shimming

> stealing info from POS systems CC Readers and ATMs

> Can be at any place
> 
>Can be overlay attachment or completement replaced device

## Refactoring

> Chaning code without modifying charcterstics
>
> Often to introduce legacy apps into new systems
>
> Can also regineer classic attack code

# Wireless Attacks

## Evil Twins

> When a wireless gateway appears to be a different identical one, but is used for spoofing
>
> Also called Rogue/Malicious Access Point

## Disassocation Attacks
> Stations used to control and management frames
>
> Access Point impersonation common
>
> Then perform DoS on infastructure
>
> Force victim to reauthenticate on your frame
>
> Use Management Frame Protection to protect yourself to drop any spoof management frames
>
> Using WPA3 mandated MPP

## Man in the middle

> Honeypot AP gets user to connect
>
> All data camptured
>
> Can be used to infect CLients with malware
>

## Jaming Attack
> form of DoS attack
>
>flood with RF to prevent traffic
>
>exploit kits have several modules and scripts
>
>Modern  APs and controllers can detect rogue APs
>
> if a rogue AP can be plotted on map

## Weak Initilization Vectors
> Deprecated bs
>
> Hackers can get challenge phrase and encrypted reponse to crack WEP
>
> Crackers decrypt catprured traffic
>
> Provides weak encrpytion
>
> initi vector is a cleartex 24bit key

* WEP Vulnerable to several attacks
> Passive attacks to decrypt traffic
> Active attacks inject new traffic from unauthorized stations using know plaintext
>
> Dictionary attacks permit real-time automated decryption of all traffic after analyzing 24 hours of frames


## WPA3 Dragonblood Attack

> Dragonfly Handshake near impossible to attack
>
> However someone within range can recover Password 
> 
>CVE 2019 13377 : timing based side-channel attack can be used
>
> WPA3 must be patched

## BlueJacking

> Old bluetooth prank
>
> Can send contact info without authentication
>
> Cracker created address book 
>
> Spoof name sent to other phone
>
> No data is stolen


## Blue Snarfing
> Stolen data form wireless device
>
> Any bluetooth set discoverable is vulnerable here
>
> It is illegal in many countries due to privacy laws

## RFID and NFC

> Data stored on RFID can be skimmed
>
> Common attacks : sniffing, spoofing, replay, mitm, clonging, dos, jammer, blcohge

# Man In the Middle Attacks

> Can be good (proxy, translators ect) or dangerous
>
> System with ability to view comms can inject iself in path 

### Man in the Browser
> Trojan horse used to capture calls between browser and sec machnisms 
>
> usage is commoon in financial fraud 
>
> can be used with other authenticating methods too

# Layer 2 Attacks

> ARP Posoning 
>
> Injects frames to corrupt ARP cache buffers on , firewalls, switches, or routers
>
> only works on IPv4
>
> Exploit kits have several tools to exploit
>
> Can be mitigated with port security, snooping binding db's on switches and MACsec  implementation 802.1AE


# DNS Attack

> Attacker uses several transparent layers to trick users into clicking a button
>
> Hijacks clicks to route to another page controllbed by another domain or app
>
> Keystrokes can also be hijacked with iframes Css and text boxes


## DNS Poisoning
> attacker changes name info that should be in DNS cache so that client systems are directed to wrong sites
>
> Accomplished through malicious exploits of DNS System

> When poisoned the DNS Server can be used for pjhishsihng and pharming

## Domain Repuation Attacks
> Monitor domain interations
> Bad domain associations (we do not want this)
> Using Pen testing and threat intel to precent bad associations

# Denial of Service Attacks

> Leverage weaknesses in TCP/IP Stack
>
> Try to consume system's critical resources

## DDoS Botnets

> Botnets are group of systems with computer robot code
>
> C&C server control to direct them
>
> Often P2P, IRC or Twitter
>
> Bots can propogate, contorl keystrokes, relay spam, open backdoors etc
>
> Usually more polymorphic than trojans
>
> Zombified systems can run hidden comms to other devices

# Malicious Code or Script Execution

## Mal Code
> From where malware derived
>
> * Virus is unwanted code that can damage system
> * Strict def is that it miust use human or system intervention to transfer
 ## Mal Script
> * Written usin scripts
> * viruses infects other scripts or form part of it
> * only affects apps for which written
> * often spread through email attachments

> Both commonly tranferred through:
> * storing data
> * attachments

