# Personnel Policies

## NDAs
- legal contract bw two parties
- Identifies confidential info
- restricts sharing
- Commonly used in interview process

## Background Checks and INvesitgaitons
![](./background.png)

## Onboarding
- Ramp up new or existing employees
- Provide assets guidance, knowledge, skills 
    - videos, printed material, CBT, etc
- Deliver sec awareness and AUP expectations
- Clearly define role
- Remove any ambiguity and uncertainy

## Automating Onboarding
- enterprises often deply systems that invovle self-service onboarding of personal devices
- emplyee registers new device, and the native supplicant is autopmatically provsioned for tha tuser, and device, and installed using supplicant profile that is preconfiguresd to connect the device to the corporate network
- offboarding is the reverse process

## Personnel Policies
- Change managemet process
- least privledge prolicy
- Mandatory policy
- Seperation duties
- Rotation of duties
- Clean disk policy
- Social Media usage

## AUP
- Condifere most improt sections
- Defines rules and behaviors
    - Language
    - illegal activities
    - avoid disturbing other systems
    - Do not reveal personal info
    - Do not reveal confidential info
- Identifies how emplyees are expected to use resources in the organization
    - Example:
        - Computer
        - mopbile device
        -sw
        - OS
        - USB
        - file transfer
        - remote access
        - telephony usage
        - Wireless LAB
        - Social Media usage
        - Cloud computing

## Standard Operating Procedure
- Step by step for carrying out tasks'
- Describe purpose and limits of procedures
- Offer all steps
-  Clarify concepts and terminology
- Consider health and safety issues
- List the location of all necessary supplmental resources

## Sec Awareness Training
- Involves steramin webinars
- Email bulleting
- Classroms
- Phishin campaings
- gamification
- Self paced training
- posters, mugs, mouse pads

> - should rep Org's misison and values
> - all applicable polcies
> - Ecamples:
>   - password and badge policy
>   - tailgating/piggy  bakcing
>   - Social engineering and phishing awareness
>   - DLP
>   - rules and regulations

## Role based Training
- General users
- Data systems and ownersd
- Data custodians
- Admins
- Privleged users
- Executive users

## Emplyee Release and Exit Interviews
- Identify factors that led employee to leaving
    - how can org improve to keep employees
- Remind exiting employee of their agreements and responsibilities
    - review NDA they signed
    - remind them o fwhat theyre forbidden to discuss with others
- Adhere to well-defined offboarding sec polcies

# Third Party Risk Management

- BPA - business partners agreement
    - purpose of business
    - contributions
    - rights and responsibilities
- SLA - service level agreement
    - official commitment beween provider and consumer
    - Defines quality 
- OLA - organizational level agreemtn
    - internal version of SLA
- ISA - interconnectionsecurity agreement
     - Documents that formalizes connections between two orgs
     - Defines security and safegaurds for the connections
     - AWS direct connect
- MOU/A - moemorandum of understandin or agreemtent
    - defines pre-agreement parameters and commitemetn bw two parties
    - generally non-binding declaration of intenet or responsibilties of each party

## Measurement System Analsysis (MSA)
- MAthematical technique for deciphering degree of deviation that occurs when using a measurement process
- Often used to endorse a measurement system by evaluating correctness precision and strength

## Third Party Risk Factors
- Vendors and supplier reliability
- Supply chain quality and security
- Business partner privacy vulerability
- End Of Life products
- End of service posture

# Data Policies

## Labeling and Classification
- also called "Sensitivity Levels" 
- USed for classification of data, information, and logical/physical assets
    - can invovle physical asset tagging and inventory systems
    - Virtual tags case sensitive key-value pairs store in config mgmt doc/NoSql DB
- Assists in detmeirning priority and protections based on risk tolerance
    - Avoidance, acceptance, etc

### Attributes for Labeling
- Monetary Value
- Age
- Utility
- Personal Association (PII,PHI)

## Classification Schemes
 ### Military
 - Top secret
 - Secret
 - Secret But Unclassified (SBU)
 - Confidential
 - Uncalssified

 ### Commercial
 - Corporate Confidential
 - Personal Confidential
 - Trade secret/propietary
 - Private
 - Public

## Handling
- contrrols who has access to info
- Can be base don 
    - class
    - sensitivity levels
    - risk treatment

## Data rols
- Owners
    - creator of data
- Steward
    - manages data or metadata from business perspective
- Custodian
    - keeper of info from tehcnical perspective
        - making sure it is available
- C-suite

## Data Retention
- Keeping data until it is not longer needed
- Policies identify how where and why data will be retained

Destruction
- Burning
- Shredding
- Pulverizing
- Pulping

Sanitaiton
- Degaussing
- Purging
- Wiping
- Encrpytion

# Credential Policies
## User Accounts

- must be unique per person and not shared
- Often use DAC security model
- Admins should have seperate non-privleged account for normal daily activities
- Best when centrally managed
- Least privledge
- MFA is prefered to simple password creds
- Employ lockout after 3-5 failed logins
- SSO should be neterprise goal

## Chared Accounts
- Anonymous or guest accounts 
- Temp employyee accounts
- Shared admin accounts
- Batch or script running accounts

## Privleged Accounts
- Accounts with elevated access to systems with special creds
- Typically given non-restricted or least elevated access to system
- Designed for SAs to deploy and manage IT systems
- Considered "keys ot kingdom" and are prime target in kill chain

### Examples of Privleged accounts
- root and privleged exec users
- Local admin accounts
- forest/domain admin accounts
- emergency accounts
    - unrpivleged users with admin access for emergencies
- Application accounts

## Service Accounts

- privledged local or domain accts for app ro svc to function with network OS
- Some domain admin privleges contrigent on app needs such as email or DB services
- local svc accts can operated w/ several different system component which renders coordination of password changes challenging
- acct passwords are rarely changed and can be significant vulenrability

# Organizational Management

## Change Management

1. Submitting
    - proposal for change management
2. Approving
    - if automated it is not applicable here
    - could be changing to new config or device
        - may be denied
3. Documenting
    - inputting changes into change log
    - must be updated regularly
4. Testing
    - not always done
5. Implementing
    - implemented after changed are green lighted
6. Reporting

## Change Control
- in ITIL 4 change mgmt called change control
- goal is maz amt of successful service and product modifications
- Assuring proper risk assessment change authorization and scheduling

## Types of Changes
- Standard Changes - low risk pre-authorized and well-documented - often svc requests that dont need addtl authorization
- Normal - follow specific process for scheduling - assement, and authroization
- Emergency
    - must be made immediately and may invovle advisory board

## Asset Mgmt
- Scope covers all HW, SW, network infastructure, endpoint devices, virtualization hypervisors, and cloud resources
    - Valuation
    - Classification
    - Labelling and tagging
    - Handling
    - Disposition

### Purpose of Asset Mgmt
- Max value
- Control costs and meet objectives
- Manage risk and slign with access control framework
- Support the decision-making process
- Meet regulatory and contractual req's

# Regulations, Standard, and Legislation

- Regulatory v Non Regulatory
    - Regulatory
        - HIPAA, SOX, GDPR
    - Non Regulatory
        - NIST, ITIL4, ISO/IEC, COBIT5, CIS, ISACA
- Country v Internation
    - US
        - FISMA, GLBA, COBIT5, HIPAA
    - INTL
        - GDPR, ITIL4, ISO/IEC, IDABC, OBASHI
- Indusstry
    - PCI-DSS for credit card companies
    - Sarbanes Oxley (SOX) for financial services
    - HIPAA for PHI
    - GDPR for EU privacy

# Key Frameworks

- help determine orgs maturity level by performing gap analysis against best practices and implementing agreed risk controls
    - CIS
    - NIST (Common secure configs)
    - Internation Organization for Standardization (ISO)
        - 27001/27002/27701/31000
    - SSAE SOC 2 Type II/III
    - Cloud Security Alliance

# Benchmarks and Secure Configuration Guides

## Benchmarks
- Tecnique to improve infosec mgmt y establishing standard
- CIS Benchmarks are best practices to config various systems
- established w/ special method from gloabl cybersec experts
- CIS Benchmarks are sec config guides created by gov, business, and academia

## Secure Confguration Guides
- During implementation phase od sec lifecycle, one will develop and implemet sec policies, procedures, baselines, and config guidelines
- info is like a standard but is more flexible and usually not mandatory

## Specific COnfiguration Guides
- Web server
    - OWASP
- OS
    - WIndows Linux, Unix, 
- App Servers
- Network infastructure



    