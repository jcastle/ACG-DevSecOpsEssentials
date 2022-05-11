# A Cloud Guru - DevSecOps Essentials

https://learn.acloud.guru/course/303a1677-0bc8-41d2-bbe0-66ae7e4e01c0/overview

## Introduction

- DevSecOps first published by Gartner in May 2016
- DevSecOps is about culture - attitudes and behavior in a social group
- Culture change is essential to sustain ongoing process improvement
- Cross functional teams must work together and everyone is responsible for security
- DevOps is not about tooling - its about process improvement
- To achieve goal of DevOps, quality software must be deployed faster
- "automate everything"
- Automation - SW version control, continuous integration, continuous testing, config management and deployment, continuous monitoring, containerization, and container orchestration
- Measuring DevSecOps
  - Deployment frequency - fast and frequent releases
  - Reduce lead time - code to cache lifecycle
  - Detection of threats, vulnerabilities, and malware
  - Mean time to repair and remediation
  - Efficiency of rollback and recovery

### Overview of DevSecOps

- Historically IT departments are separate - dev, security, and ops. Dev for app development, security for regulatory governance and compliance, and ops for maintaining data center infrastructure.
- Security monitoring - applications continuously monitored for vulnerabilities, often require refactor based on dependency library
- Release and adapt - performance often prompts subsequent iterations of software enhancement; adjust culture over time based on KPIs, supports faster time to market

### Cybersecurity Concepts - Part 1

- Attack surface and attack vectors
- Malware - malicious SW attackers use to attack individual computers
- Vulnerability - weakness in the system where malware can be introduced
- Open SCAP Project - collection of open-source tools for implementing and enforcing SCAP (NIST standard)
- Center for Internet Security - cookbooks for hardening developed by NIST
- Scanners - can monitor on hosts and in real time
  - Dynamic scanning - identifies vulnerabilities in a runtime environment
  - Static scanning - performed in non-runtime environment
- Cloud Security Alliance - consolidated most security compliance methods into the Clouds Control Matrix (CCM). CCM includes controls such as ISO, FedRamp, and NIST 800-53.
- Open Web Application Security Project (OWASP)
- Federal Information Processing Standards (FIPS)

### Cybersecurity Concepts - Part 2

- Common Vulnerabilities and Exposures (CVE)
- National Vulnerability Database (NVD)
- National Checklist Program Repository

### Identity and Access Management

- DevSecOps Pipeline Flow security - Server hardening, application hardening, and identity and access management
- IAM - process of granting or restricting access to users and groups

## Secure Software Onboarding

- Process developers use to acquire third party components needed to develop and compile an application

### Clean Repositories

- Attack vectors are often exploited in public systems
- Use firewalls for on-prem resources, use scanning for onboarded SW
- PaaS requires repository hardening

### Securing Public Repositories

- Hackers can study public source code to learn how to exploit the SW
- Hackers can look for vulnerabilities that are more difficult to detect through the penetration of production systems
- Login credentials - embed login credentials in the code itself; microservice architectures increase attack vectors w/ login credentials (12 factor app, store env and login credentials on prompt or through .git ignore)
- Insider threats - a single developer accessing many repositories or code bases; no monitoring of GH repos over time
- Practical DevSecOps to tighten security w/ public repos
  - Clean up login credentials, limit access, revoke credentials when individuals leave project/company
  - Maintain repo settings - treat all GH as open source repos, consider the community
- Security requires effort

### Secure Containerization

- Containers - formatted files that contain executable application programs, modules, and the code libraries they depend upon
- Docker Hub - collection of images - public, private, and official

### Docker Trusted Registries

- Trusted registries are secure managed repositories
- A registry is the data store that contains metadata
- Trusted registries use digital signature
- Trusted registries key to trusted automation
- Docker uses private keys to sign containers

### Docker Bench

- SW tool that analyzes server infrastructure and Docker components
- Uses CIS Docker Benchmark
- Dock Swarm is a native clustering solution from Docker that can be used for container orchestration
- TUF (Trusted Update Framework) used to enforce content trust
