# Authentication Authorization and Accounting (AAA Services)

## Authentication

- Validating something/someone is who or what they claim
- Passwords are most common but getting augmentated/replaced
- Authentication can be in multiple layers
    - origin first, followed by more advanced forms
    - not identification, since password or key gives authetication, not the ID

## Authorization

- process of granting entity permission to access 
- access control/client privledge/subject sensistivity level
- in a secure environment, although authorization is technically optional, it must always follow authentication

## Accounting

- Also optional
- Reasons:
    - Billing and Chargeback
        - different departments responsible for stayin in budget
        - provide visibility on cost
        - Showback offers management of IT costs due to each department without cross-charing
        - RADIUS and DIAMETER are popular tools
    - Auditing and Reeporting
        -    used to audit usage of resources for securitty and operational reasons
        - may be part of governance like GDPR or HIPPA

# Character Mode v Packet Mode

- Couple of ways to approach AAA

## Character Mode

- sends keystroked through networked devide (often with RADIUS or TACAS+) through the TTY vty AUX or CON ports
- purpose of configuration or query commands ON the Device

## Packet Mode

- Uses interface or link protocol  session to comm with device on other side of authenticatin device
- Also called network mode since AAA is being used to grant access to server or network

# Directory Services

- vital to AAA system for the SMB to large enterprise
- hierarchical structure that stores data about network objects
- Active Directory Domain Services (AD DS) is one of world's most popular and stores usernames, passowords, Phone numbers, devices and more
- allows other authorized users and systems on the same network to access information

## Active Directory Componenets

- Set of rules called **Schema**
    -  Also has other info like limits
- A global catalog of all objects
    - can give that info across domains
- A query and indexing service
    - mechanisms so object and attributes can be found by users
- A replication service for data distribution
    - Domain Controllers that handle distributing the copies of the same info to all systems in domain
- LDAP 
    - often provide access for management apps and browsers that need interavtive read/write acces to an X.500 or AD service
    - AAA systems can leverage existing user repos for authentication
        - AD uses KErberos and ticket granting service
    - If LDAP is used, systems can offer user repos with sophistacted password managemetn to AAA front end

## Securing the Directory

- attackers can
    - steal data, modify docs
    - impersonate users
    - Disrupt business ops
- need to have MFA, protect privleged accounts, admins and servers 

- Have seperate admin accounts
- Just in time local admin passwords
    - in case they try to steal it from hash
    - LAPS is usually used to configure hashes for seperate machines
- Implement Azure Advanced Threat Protection (ATP) in teh clous
- Enable MFA for all admin accounts
- Secure all data in transit 
    - IPSec TLS etc


# Federation and Attestation

- Federation is trust between different domains
- When federation standards mattured, orgs developed/adopted federation networks where identity info can flow between institutions
    - Identity org then **Attests** identity of users
- Federation involves identity providers, truster service providers, and attestation using assertions or tokens

## Single Sign-on

- when CSP users habe lots of IAM accounts, you can use federation to authentication

## AWS Cognito
- also does federation with cognito sign in
    - You can have people register with your app and populate info into a user pool
    - can use third party accounts like Amazon, Apple, Facebook etc


# Authetnication technologies (2FA)

- when we add something to user/password combo

> - Time based one-time password (TOTP)
>   - During authentication you put in digits that appear
>       - Yubi-key is another popular one
>   - Can also be digital token
>       - like DUO or google authenticator
> - HMAC-based one-time password (HOTP)
>   - symmetric creation of human readable values, but only vaialble one time 
> - SMS
>   - when they text
> - Token Key
>   - not really used much anymore.
> - Static codes
>   - a static code you create
>   - long string
> - Authentication Application
>   - register all sites and creds into app and you use one master password
> - Push notifications
> - Phone calls 


# Smart Card Authentication

- special form of 2FA
- Connect smart card to host PC
- Can also be used to authenticate access to building
- SW on laptop interacts with keys and/or secrets
- Info is stored on card
- Common Access Card CAC is a common one

## CAC
- Shows active duty guy with:
    - Expiration date
    - identifier
    - Affiliation
    - Color
    - Pay grade
    - Rank
    - Integrated Circuit Chip

# Biometrics

## Fingerprint Biometrics

- Most common since they vary and do not change
- Integrated into mobile devices 
- has two functions:
    - get image of finger
        - will not be saved, only grab binary code
        - saved as key
    - detmerine whether outline ridges in the image matches pattern

## Facial Recognition
- Common to verify in Still or Video images
    - popular because not intrusive
- main application is security biometrics and HCI
- Main method for modeling is Principal Component Analysis (PCA)

## Retinal Scans
- Oular based tech
- retina is thin tissue at back of eye
- each persons retina is distinct
- scanner sends beam into eye, reflection calculated and senses
- considered invasive

## Iris Scan
- Thin circular color part of eye
    - controls size of pupil
- muscles expand/contract pupil
- iris scnners use camera tech to sense differnces

### Similarities

- low rate false positives and exrtremely low rate of false negatives
- reliabiltiy because no two people have same eye patterns
- identity of subject can be rapidly confirmed
- cappilaries decompose too faqct to use a removed eye for access

### Differnces
    - retinal scan can be affected by disease but iris stays constant
    - iris scan noninvassive 
    - iris scans more accepted commercially

## Voice Recognition
- diffs in speaker recogntion and speech recogntion
- voice recog used for both
- Speaker recogition leverages aural aspect of speech
- Traits include human physical stucture
- Voice recog is classified as "behavioral biometric"

## Vein and Gait Analysis

- Vein pattern recog comes in:
    - Palm vein 
    - Finger vein
        - both palm and finger use near infrared
    - Retina vein 
- Gait Biometrics identify people based on their unique walking pattern
    - has advantage of being unobtrusive and requires no contact

## False Acceptance Rate

- Measure probability that system will incorrectly accept effort 
    - FAR is number of false accept / amt of auth attempts

## False Rejection Rate

- mearsure incorrectly denies

## Crossover Rate

- Crossover error rate CER is value of FAR and FRR when the sensitivity is setup so that FAR and FRR are the same
    -   excellent for quantitative comparison of differing biometrics

# Multi-factor Authentication (MFA)

- involves 2 or 3 factors (sometimes more)
    - Something you know (password or passphrase)
    - Something you have (smart card, token, CAC)
    - Something you are (biometrics)
    - Attributes (ABAC) [attribute based access control]
        - Somewhere you are
        - Something you can do
        - Something you can exhibit
            - takes credentials and create temp badge

# Cloud v On-premise requirements

## Cloud Provider

- Concern is only at Layer 3 and above
- RDP over TLS or other authentication
- Identity Access Management and or SSO
    - in Azure it is AD
- Programmatic or Console Access
    - can be network or character mode
- Share responsibilty based on level of managed service
    - accounting and visibilty is usuualy relying on cloud

## on-premise

- must include physical sec from layer 2
- more control over access model
- more flexible protocol and solutions


