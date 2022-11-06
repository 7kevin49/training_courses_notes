# Virtualization Basics and VM Security

## VMs
- running virtual OS isntances
- refers to above
- to Applications running on top of virtualized machine, seems as though they are on their own deidicated OS

## Hypervisor
- SW that gives virtual infastructure
- Resource traffic cop b/w cirtual components
- How much access they get is maanged here
- Host runs hypervisor
- guest gets resources

## Type 1 Hypvisor
- Built directly on hardware
- ESXi, Hyper-V, OVM, Fusion Sphere
    - OSS --  KVM, open VZ, redhat

## Type 2 Hypervisor
- Hypervisor is installed on host OS
    - VMWARE, or Virtual Box

# VM Vulnerabilities
- VM Sprawl
    - VMs overtake admin's ability to manage VMs and available resources
- Avoidance
    - Strict process for deploying VMs
    - Library standard of VM images
    - Archive under utilized ones
- VM Escape
    - Guest VM process interacts with Host
        - More often in Type2
    - Protection:
        - Patch SW regularly
        - Install only what you need
        - Strong system security (passwords and access)

# Cloud Models

## Cloud Computing Value Propositions
- Cost savings and resource pooling
- Rapid elasticity and agility
    - easier for rapid deployment
    - also gives auto scaling
- On-demand service with broad access
    - AWS broad service and availability
- Measured services w/ visibility
- Security and shared responsibility

## Cloud COmputing Service Types

### Infastructure as a Service
- provision processing, storage, networks, and other resources so consumer deploys/runs sw.
- Consumer does not manage or control cloud infastructure
    - but does control OS, storage and configurations
- customer spins up infastructure
- AWS, Microsoft Azure are examples

### Platform as a Service
- Condumer deploys apps using languages form the provider
- Consumer does not control underlying infastructure, but does have control over deployed apps and possible host configurations

Common Paas Services include:
> - SDK's
> - COntainers
> - DBs
> - Threat intel
> - sign in services

### Software as a Service
- use provider's app on cloud. 
- Accessible through different deviced
- Consumer does not maange anything except maybe user-specific app configs

Examples include:
> - CRM
> - wokrplace tools
> - finance tools

## Cloud Models
- Private - deplyed in sandbox within an org 
- Public-  deployed by provider for customer consumption
- Community - deployed by a group in a sector
    - partners in busines sector
- Hybrid - combination of private, public, or community

# Cloud Service Proviers Concepts

## AWS Service Offerings
- Archiving
- Backup and Restore
- Blockchain
- Business apps
- Cloud Migration
- Containers
- Content Delivery
- Database Migrations
- Data Lake and analytics
- DevOps
- E-Commerce
- High Performance computing
- Hybrid Cloud Architectures
- Internet of Things
- Machine Learning
- Mobile services
- Modern application development
- Remote work and learning
- Scientific Computing
- Serverless Computing
- Websites

## Managed Security Service Provider (MSSP)

- outsources security mointoring
- Apply to on premise and cloud or btoh
- Common services:
    - layer 3-7 Firewalls
    - IDS/IPS
    - Enddpoint response and detection
    - Cirtual private networking support
- user high-availability op centers
- offer 24/7 services w/ goal of reducing on-premise operational security staff the enterprise needs to hire, triain and retain to preserve security


