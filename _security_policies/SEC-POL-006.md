---
title: Remote Work and Cloud Security Policy (SEC-POL-006)
parent: Security Policies
nav_order: 6
---
### 1. Objective

The objective of this policy is to establish comprehensive security requirements for **ASM One Inc.**'s remote workforce, endpoint devices, and cloud infrastructure oversight. As a fully remote, cloud-native organization, this policy ensures that appropriate safeguards are implemented to protect company equipment, secure remote work environments, and validate cloud provider security controls while maintaining the confidentiality, integrity, and availability of information assets and electronic Protected Health Information (ePHI) in compliance with HIPAA, HITECH, and SOC 2 requirements.

### 2. Scope

This policy applies to all **ASM One Inc.** workforce members, contractors, and third parties who access company systems or handle company equipment. It encompasses all remote work locations including home offices, co-working spaces, and any location where company information is accessed or processed. This policy covers all endpoint devices including workstations, laptops, and mobile devices, as well as the oversight and validation of cloud provider security controls for infrastructure hosting company data and systems.

### 3. Policy

- **ASM One Inc.** shall implement layered security controls appropriate for a remote-first, cloud-native operating model while ensuring comprehensive protection of all endpoint devices and validation of cloud provider security.

#### 3.1 Remote Work Environment Security

All remote work environments shall meet minimum security requirements to protect company information and systems.

##### 3.1.1 Home Office Security Requirements

- **Workspace Security:**
    - Dedicated workspace with measures to prevent unauthorized access to screens and equipment
    - Privacy screens or positioning to prevent visual access to company information by household members or visitors
    - Secure storage for company equipment when not in use
    - Locking mechanisms for storage areas containing any physical company materials

- **Network Security:**
    - Secure Wi-Fi with WPA3 or WPA2 encryption and strong passwords
    - Router firmware kept up to date with security patches
    - VPN required for all access to company systems and data
    - Prohibition of accessing company systems on public or unsecured networks without VPN

- **Environmental Security:**
    - Protection of equipment from environmental hazards (water, heat, pets)
    - Adequate power protection (surge protectors recommended)
    - Secure disposal of any printed materials containing company information

##### 3.1.2 Public and Shared Space Restrictions

- **ePHI and Restricted Data:**
    - Processing of ePHI or Restricted information is prohibited in public spaces (cafes, airports, co-working spaces)
    - Privacy screens required when working on Confidential information in any shared environment
    - Voice calls discussing sensitive information prohibited in public areas

- **Device Security in Public:**
    - Devices shall never be left unattended in public spaces
    - Screen lock shall be engaged immediately when stepping away
    - Bluetooth and AirDrop shall be disabled when not in active use
    - Shoulder surfing awareness and positioning required

#### 3.2 Endpoint Device Security

All company equipment and endpoint devices shall be protected against theft, damage, and unauthorized access throughout their lifecycle.

##### 3.2.1 Device Protection Requirements

- **Physical Device Security:**
    - Full disk encryption required on all devices (FileVault, BitLocker, or equivalent)
    - Remote wipe capabilities enabled and tested for all mobile devices and laptops
    - Strong authentication required (biometric or complex passcode)
    - Automatic screen lock after 5 minutes of inactivity maximum

- **Device Configuration:**
    - Mobile Device Management (MDM) enrollment required for all devices accessing company systems
    - Automatic security updates enabled where supported
    - Only approved applications from company software catalog
    - Local firewall enabled on all devices

##### 3.2.2 Device Lifecycle Management

- **Provisioning:**
    - Secure provisioning process with pre-configured security settings
    - Asset tagging and inventory tracking for all company equipment
    - MDM enrollment verification before access to company resources

- **Ongoing Management:**
    - Quarterly compliance verification through MDM
    - Regular security posture assessments
    - Prompt reporting of lost, stolen, or compromised devices

- **Decommissioning:**
    - Secure data destruction with verification before device disposal or reassignment
    - Certificate of destruction for devices containing ePHI
    - Proper disposal of devices through certified e-waste recyclers

##### 3.2.3 Removable Media Security

- **Usage Restrictions:**
    - Use of removable media (USB drives, external hard drives) for company data requires approval
    - All approved removable media must be encrypted
    - Removable media containing ePHI prohibited except for approved backup procedures

- **Secure Disposal:**
    - Secure deletion required before disposal or reassignment of any removable media
    - Physical destruction for media that contained ePHI or Restricted information

#### 3.3 Cloud Provider Security Oversight

**ASM One Inc.** shall validate and monitor the security controls implemented by cloud service providers to ensure appropriate protection of company data and systems.

##### 3.3.1 Cloud Provider Assessment

- **Security Requirements for Cloud Providers:**
    - SOC 2 Type II certification or equivalent demonstrating security controls
    - Multi-factor authentication and strong access controls for data center facilities
    - 24/7 security monitoring and surveillance systems
    - Environmental controls including fire suppression, climate control, and power management
    - Geographic separation of data centers for disaster recovery and business continuity
    - Encryption of data at rest and in transit

- **Compliance Validation:**
    - Annual review of all critical cloud providers' security certifications (SOC 2 Type II, ISO 27001)
    - Review of third-party audit reports and security assessments
    - Contractual requirements for security standards and incident notification
    - Right-to-audit clauses in contracts for critical cloud services where feasible
    - Geographic data location controls aligned with legal and regulatory requirements

##### 3.3.2 Cloud Security Monitoring

- **Ongoing Oversight:**
    - Quarterly review of cloud provider security incident reports and notifications
    - Continuous monitoring of cloud provider security advisories for significant control changes
    - Annual assessment of cloud provider business continuity and disaster recovery capabilities
    - Validation that data center certifications and compliance status remain active
    - Coordination with cloud providers for security investigations and incident response

- **Cloud Configuration Security:**
    - Infrastructure-as-Code for consistent and auditable cloud configurations
    - Regular security assessments of cloud resource configurations
    - Automated compliance monitoring for cloud security baselines
    - Access logging and monitoring for all cloud administrative activities

#### 3.4 Information Handling in Remote Environments

Information shall be protected appropriately in all remote work contexts.

##### 3.4.1 Digital Information Security

- **Data Protection:**
    - All company data shall be stored in approved cloud systems, not on local devices
    - Encryption required for any data temporarily stored locally
    - Regular backup verification for cloud-stored data
    - Secure file sharing only through approved platforms

- **Communication Security:**
    - Encrypted communication channels required for all business communications
    - Approved video conferencing platforms only for meetings involving sensitive information
    - Screen sharing awareness—verify attendees before sharing sensitive content

##### 3.4.2 Minimal Physical Document Handling

- **Paper Document Policy:**
    - Digital-first approach—avoid printing sensitive information when possible
    - Any printed documents containing Confidential or Restricted information shall be:
        - Kept secure and not visible to unauthorized persons
        - Shredded or securely destroyed when no longer needed
        - Never disposed of in regular trash

#### 3.5 Security Awareness and Responsibilities

All workforce members shall understand and fulfill their security responsibilities in remote work environments.

##### 3.5.1 Workforce Security Requirements

- **Security Training:**
    - Annual security awareness training including remote work security procedures
    - Role-specific training for handling ePHI and sensitive data remotely
    - Incident reporting procedures for security concerns or breaches

- **Compliance Responsibilities:**
    - Maintain secure home office environment meeting policy requirements
    - Report any suspected security incidents or device compromises immediately
    - Participate in security assessments and compliance verification activities
    - Keep devices updated and compliant with security requirements

##### 3.5.2 Incident Reporting

- **Reporting Requirements:**
    - Lost or stolen devices shall be reported within 1 hour of discovery
    - Suspected security incidents shall be reported immediately to security@trycoral.ai
    - Workforce members shall cooperate with remote device wipe procedures when required
    - Documentation of incident circumstances shall be provided as requested

### 4. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Security Officer**|Develop remote work security policies, oversee cloud provider security assessments, coordinate with IT for endpoint security, and ensure compliance with security standards.|
|**IT Security Team**|Implement and manage MDM systems, configure endpoint security controls, monitor device compliance, respond to security incidents, and maintain cloud security configurations.|
|**Cloud Security Team**|Assess cloud provider security controls, monitor cloud security compliance, review provider certifications, and coordinate cloud security requirements.|
|**Human Resources**|Communicate remote work security requirements during onboarding, coordinate with IT for device provisioning and return, and support security training initiatives.|
|**All Workforce Members**|Comply with remote work security policies, maintain secure work environments, protect company equipment, complete required security training, and report security incidents promptly.|
|**Managers/Supervisors**|Ensure team compliance with remote work security policies, support security training completion, and coordinate device management for their teams.|
