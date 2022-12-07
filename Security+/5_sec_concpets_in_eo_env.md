# Change and Config Management

## Configuration Management
4 CI's - Configuration Items - items changed or managed to provide service

> 1. Diagrams and Topologies
>       - templates 
> 2. Baselines
>       - Config Management baselines -- for proper change management
> 3. Configuration Schemas
>       -  ie Database Schemas
> 4. Naming/ Tagging
>       - either physical or logical metadata

## Change Mangement
- Change control practice
- **Goal** - max amt of succefssful service/product changes
- should:
    1. certain risks authorized and and managed w/ change schedule
    2. Involve change log (or register, db etc (Key Value NoSQL))

## Change Management Lifecycle

1. Submitting
    - proposed change analyzed and validated
        - if necesasry, needs to be reviewed
2. Approving
    - Change request delivered to group responsible for change management
3. Documenting
    - after approval, inputed into a COnfiguration Management Databse (CMDB)
4. Testing
    - formal testing for modifications to be made if issues arrise
    - ususally for bigger changes
5. Implementing
    - deployed based on schedule determined
    - change could be automated
    - lots of automated changed part of orchestration system
6. Reporting
    - full report of change submitted to maangement
    - negative consequences result in rollback 

# Data Sovereignty

- These issues arrive when storing sensistive data by region
- Ownership/custodianship etc agreed by all legal directives
 
 > - mandates bagan during cold ware to control transborder flow
 > - ITAR internation traffic in arms regulations
 >      - applies to military/defense
 > - Export Administration Regulations (EAR) for commercial stuff or military use

## Cloud Computing Geolocation
- Sometimes data in the cloud can change countries
- Because of this, some orgs may need to restrict what servers are used
- Some policies require that data stays in same region/country
- traditional geolocation not secured, must have policies thought out

# Data Protection
- Intial steps:
    - labeling
    - handling
    - least privledge access
- diff controls used for:
    - data at rest (storage)
    - in transit
    - in use (in memory) / processing
- tokenization of mobile devices and handhelds can lead to data loss or leakage
    - enterprise mobility management

## Data loss prevention DLP

- manages loss/leakage of data beyond domain
    - IP, secrets, campaigns etc.
    - PII
    - PHI
- may involve masking/stripping out info (redaction) or enctyption.

Steps:

1. Data
    - above mentioned
2. Can Leak
    - on network
    - copied on removable media
    - transmitted
3. To an outsider
    - any unauthorized entity
4. Resulting in breach
    - defmaation
    - monetary expense
    - customer trust breached
    - potential closure of business

## Digital Rights Management
- used to protect propietary hardware and copyrighted work
- attempt to manage use, modification, distribution of copyrighted software and multimedia

# Hardware Security Modules (HSM)
- dedicated cripto processors consisting of hardnedd, tamper-resistant devices and virtual appliances for key management

- manage, process, generate, and store PKI, SSH and trusted platforms

- verify digital certs. enscript and decrypt and verify integrity

> - SSL Accelarators that offload public-key processing
> - Cyber Crypto exchanges use them to store client blockchain
> - Foundations of a trusted Execution Environment or Trusted Computing (TC) use these crypto processors as prt of trusted model

# Geogrphical Considerations
> - Where to store offiste data and backups
>   - distance - city, state, country, cloud
>   - Cloud HSM may not be allowed, HSM may be required on-site
>   - location selection - can we operate or store there?
>   - sec standards
>   - data soverignty
> - Local geographic restrictions on mobile devices
> - Automobiles stopped by geofencing

Things to consideration:
> - Jurisdictions
> - Privacy laws
> - Import/Export
> - Cryptography

# Cloud Access Security Brokers
> - Software service implemented b/w cloud customer and Software as a Service provider (Salesforce etc)
> - could be on premise or in-service
> - Act as gatekeepr to enfore policies while services accessed

> - extend policies beyond local infastructure
> - provide visibility, compliance, data sec, and threa protection

# Response and Recovery Controls

## Risk Response

- Accept
    - means dont implement safeguards
    - get justification in writing
- Mitigate
    - reduce risk exposure
- Transfer/Share
    - Insurance/service provider
- Avoid
    - do not take action that introduces risk

> - Sec Guards are critical response control
> - can be deterrent
> - COnsiderations
>   - hire or contact
>   - armed/unarmed
>   - screening
>   - training
>   - Impact on insurance

> - Computer Sec Insident Response Teams (CSIRT)
>   - internal team or third party
>   - providee 247 response
>   - deliver single POC for sec incidents
>   - will be 1st responders in many situations and can be involved in computer forensics

## Common Recovery Control Acticities

- Data recovery
- mobile device location and wiping
- Developing/testing business continuity and recovery plans
- Determining RTO and RPO metrics for business impact analysis
- Finding best disasater recovery site solution

# SSL TLS 

- inspection involves hardening all web services responding to HTTPS clients on internet and in private networks
- comprises the deployment of web app firewalls and deep packet inspection 
- Managed Security Service Providers (MSSP) can do this

## TLS BEst practice
- up to date sec
- make sure browsers are updated
- dont let vendor installed code intercept traffic
- ensure client computers are malware free
- perform revocation checks
- verify that encryption is being done
- check certificate expiration dates
- get TLS erts from trusted sources
- emply pinning and OCSP stapling
- Deplot HSTS protocol server side

# Hashing and API Considerations

## Hashing
- Cryptographic hashes are only hald the key strength due to birthday paradox
- Older MD5 and SHA-1 should be avoided
- consider using elliptic curve Diffie Hellman and foward secrecy
- AES-256-GCM has built in hash authnetication

## API
- Digitially sign all API calls
- DO not embed credentials in an API call
    - same thing for keys
- Only connect to trusted sourced
    - ie Cloud Providers
- Protect secret keys used for APIs
- Deply secure coding practices

# Site Resiliency 
- Resiliency is capability of server/network/db/or storage to recover and continue ops when failure/disruption happens
- Common term is site resilience and it refers to durability and high availability

Some options:
- Cold site
    - HVAC enabled and with networks
    - can take 24 hours to move to
    - Some times dont even have ethernet points and rely on wireless
    - after disaster its where everythign gets moved to
- Warm Site
    - have things in there like racks or other hardware
    - very likely to have HVAC, power and HVAC
- Hot Site
    - runs in parallel
    - Where it will only take and hour to get up and running
- Mobile Site
    - some orgs rely on it 
- Hybrid Cloud
    - redundancy that is up in the cloud 
- Important for small-to-medium businesses to have a way to recover.

# Deception and Disruption
- Related to inicident response
- **Honeypots** and evil twins are used in wireless networks to trap potential attackers and as a man-in-the-middle attack
- For someone with beyond script-kiddie skill to be able to get in
- **Honeynets** are entire physical/virtual subnets used to entice attackers for gathering intel and counter attacks
- **Honeyfiles** or honey tokens are most often used to catch a privleged insider during a structured attack
- All of these are part of active defense
    - after trapping, you can try to figure out who attacker is, their attacker, and even location
    - some locations have red teams that will attack back
    - has legal ramifications


## Fake Telemetry
- Deception become a tool
- involves augmenting existing tools in enterprise to offer critical threat intelligence for early breach detection and high-fidelity alerting
- often a fake layer of infastructure with decoys and traps
- no system or person should ever access fake unless actively seeking or miconfiguration

## DNS Sinkhole
- threat analysts can use this to mointor and analyze suspicious traffic
