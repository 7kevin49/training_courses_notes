# Categories of Controls

## NIST SP 800-53 Controls

1. Mangerial
2. Operational
3. Technical

### Managerial

> - admin controls
> - should be published
>   - risk assessment/management
>   - password policies
>   - Screening/hiring etc 
>   - Training + awareness

### Operationaal Controls

> - Change and config managmeent
> - Conducting awareness and training
> - Implementing physical controls
> - contigency planning
> - Incident response
> - System and data integrity mechanisms
> - Mobile device and app management
> - Disaster recovery plan testing and drills 

### Technical Controls

> - Sec mechanisdm that specific systems run
> - Deliver Confidentiality, Integrity, AUthenticity and Availability protection
> - Defend against unauthorized access
> - Facilitate detection of sec violations

Common examples include:
- infastructure hardening
- IAM
- Key maangemenet
- Threat modeling

# Types of controls

5 Key types:
1. **Preventative** - counter measures that prevent attacks *IE IPS*
2. **Detective** - giving visibility when attack happend
3. **Corrective** - gives correction actions to correct problems after detection
4. **Deterrent** - discourage the attack - like warnings about attacking the system
5. **Compensating** - assists other controls you have in place 

# Secure Application Environments

Steps in Apps:
1. Development
2. Testing
3. Staging
4. Production
5. Quality Assurance

> - Secure by design
>   - Custom or outsourced app is developed with security integrated
>   - Attackers cannot overcome sec controls eben if they have white/gray box
>   - example: using virtual private cloud solution at AWS, GCP, or Azure

> - Secure by deployment
>   - not with security integrated, but deployed in environment where secur8ity was considered in network and system design
>   - example: air-gapped from untrusted networks (private or on-premise cloud)

> - Secure by default
>   - design assumed that app is secure w/o modification or controls
>   - Example: server app has possible unsecure functions, but disabled at deployment based on infastructure as code

# Provisioning and Deprovisioning

When provisioning, API deployment and provisioning introduces security risk

> - Can involve providsing or removing SW access to stakeholders on an as needed basis
>   - want to avoid access creep
> - in modern environments, involves autoscaling from CSP to take advantage of cloud elasticity

## Proviosingin Deprovisioning Enablers:

1. Inastructure as Code and automation
2. Auto scaling
3. VM and containers
4. Rapid deployment using Agile, Spiral, and CI/CD
5. "Hybrid as cloud" solutions

# Integrity Measurement

Secure BIOS is extremely important and thus:
> - NIST SP 800-155 - BIOS Inteegrity MEasurement Guidelines
> - Checking for digitally signed code and programs 
> - Using Linux IMA (integrity measurement architecture) subsytem
> - Implementing Trusted Computing Base solutions (TPM)
> - Server-side v Client-side execution validation

## Example

> - WS-Security (WSS) is a SOAP extension used to enforce web confidentiality and integrity security
> - memned oif Web Service specifications and published by OASIS
> - protocol specifies how integrity and confidentiality can be enforced on messgs and allows comms of various security token formats like : SAML, Kerberos and X.509

# Secure Coding Techniques

1. Normalization
  -   making sure all input is correct as it enters the system
    - no redundancy in data
    - can also be de-duplication (remove duplicate code as well)
2. Camoflauge/obfuscation
    - making things harder to understand
3. Remove dead code
4. Memory management
    - making sure appropiate access to mem is done 
    - mem leak and overflow could be bad for you
    - nx/xn bits can be counter for buffer overflow
5. Data exposure
    - dont expose backend data
6. Stored Procedures
    - use pre-compiled code where you can is secure

Also be aware of using 3rd party software as well

## Data Exposure

- Tend to abstract original data whenever possible
  - Never access original files, access cache versions at edge (not from directly on S3)
- What data can be shared or exposed to external parties
- Strict access controls and least privilege are key
- Digitally sign all API calls to data at rest
- Employ DLP engines
  - for countering data leakage or data loss

# OWASP for App Development

- Open Web Application Security Project (OWASP)
  - non profit for security in sw and apps
- OWASP seeks to enhance security understanding

> - OWASP Modible Security Testing Guide is a comprehensive publuication for mobilee app security testing and revers engineering of iOS and Android platforms
> - OWASP top 10 is also used a lot and shows consensus of most critical secuyrity risk to web apps

# Software Diversity 

- methodolgy where two or more functionally duplicate versions of app are developed from same specification
- process uses different teams
- better error detection, improved consistency, and fewer programming errors
  - downside being that you need double resources
- End-user apps are written in langfuages liek Java
- OS and dirmware support libraries, VMs are still on Low-level languages that place flexibility and performance over security
- programming errors in low-levels make apps more vulnerable
- Automated SW diverisyt techniques use ranomization to increase difficulty of sploiting hude amounts of low-level code
- Diverisyt based defense are assuming that single attack will fail against multiple targets with unique attack surfaces

# Automation and Scripting

- Continous Monitoring
  - improtant to give feddback to different teams at different points of process
- Continous Validation
  - looking for vulenrabilites, license risks, bugs, other issues
  - should be performed throughout CI/CD pipeline
- Continous integration
  - various tools to do static code analysis tests
- Continout Delivery
- Continous Deployment