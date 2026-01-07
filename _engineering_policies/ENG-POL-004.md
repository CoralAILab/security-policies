---
title: Network Security Policy (ENG-POL-004)
parent: Engineering Policies
nav_order: 4
---
### 1. Objective

The objective of this policy is to establish comprehensive security requirements for the design, implementation, operation, and monitoring of **ASM One Inc.**'s network infrastructure and communications. This policy ensures that all network components including perimeter security, internal network segmentation, and network traffic monitoring are configured and managed with appropriate security controls to protect the confidentiality, integrity, and availability of data in transit and electronic Protected Health Information (ePHI). This policy addresses network-level security controls, traffic monitoring, intrusion detection and prevention, and network access management while maintaining compliance with HIPAA, HITECH, and SOC 2 requirements. Note: ASM One Inc. operates as a fully cloud-native organization without physical office infrastructure; wireless network and guest network controls are not applicable.

### 2. Scope

This policy applies to all **ASM One Inc.** workforce members, contractors, and third parties involved in the design, deployment, configuration, or management of network infrastructure and communications. It encompasses all network components including routers, switches, firewalls, network security appliances, VPN concentrators, and network monitoring systems. This policy covers all network environments (production, staging, development, testing) and connection types including remote access connections, site-to-site connections, and cloud network services. It applies to cloud-based networking services including Virtual Private Clouds (VPCs) and software-defined networks.

### 3. Policy

- **ASM One Inc.** shall implement comprehensive network security controls across all network infrastructure to ensure secure data transmission, prevent unauthorized network access, and maintain regulatory compliance through defense-in-depth network protection strategies.

#### 3.1 Network Security Architecture

A comprehensive network security architecture shall be implemented to provide layered protection against network-based threats and unauthorized access.

##### 3.1.1 Network Segmentation and Micro-Segmentation

- **Network Segmentation Strategy:**
    - Production, staging, development, and management network separation
    - Application-tier segmentation (web, application, database layers)
    - Security zone implementation with different trust levels and access controls
    - DMZ (demilitarized zone) for external-facing services and applications
    - Management network isolation for administrative access and monitoring

- **Production Network Isolation:**
    - Dedicated VLANs or VPCs for production, staging, development, and management networks
    - Inter-VLAN routing restrictions with explicit allow rules only
    - Production database isolation with application-layer access controls
    - DMZ implementation for external-facing services with restricted internal access
    - Network address translation (NAT) and firewall controls for internet access

- **Micro-Segmentation Strategy:**
    - Application-tier segmentation isolating web, application, and database layers
    - East-west traffic inspection and filtering between network segments
    - Zero-trust network access implementation for privileged users
    - Software-defined perimeter (SDP) implementation where technically feasible
    - Container network policies for microservices isolation

- **Segregation Monitoring and Enforcement:**
    - Continuous monitoring of network traffic between segments
    - Automated violation detection and remediation for unauthorized cross-segment communication
    - Regular testing of segregation effectiveness through penetration testing
    - Documentation and approval required for all cross-segment communication
    - Quarterly review of network segregation policies and implementation

- **Security Zone Access Controls:**
    - **Internet Zone**: External internet access with full inspection and filtering
    - **DMZ Zone**: External-facing services with restricted internal network access
    - **Internal Zone**: Corporate network with standard access controls and monitoring
    - **Restricted Zone**: High-security network segments with enhanced access controls
    - **Management Zone**: Administrative network with privileged access and monitoring

##### 3.1.2 Traffic Control and Network Filtering

- **Traffic Control and Filtering:**
    - Default-deny network access policies with explicit allow rules
    - Application-layer firewalls and web application firewalls (WAF) deployment
    - Network traffic inspection and filtering for known threats and malicious content
    - Rate limiting and DDoS protection for internet-facing services
    - Network access control lists (ACLs) and security groups for granular traffic control

#### 3.2 Network Security Monitoring and Detection

Comprehensive network security monitoring shall provide real-time threat detection and rapid response capabilities across all network infrastructure.

##### 3.2.1 Network Security Monitoring Implementation

- **Cloud-Native Security Monitoring:**
    - Cloud-native security monitoring services (AWS GuardDuty, Azure Sentinel, GCP Security Command Center) shall be configured to automatically monitor VPC flow logs, DNS logs, and network traffic for suspicious activities
    - Managed Security Service Provider (MSSP) shall provide 24/7 network security monitoring, threat analysis, and incident response capabilities with HIPAA/HITECH compliance and HITRUST CSF certification
    - Cloud security monitoring tools shall be integrated with MSSP SIEM platforms with automated log forwarding and proper data retention

- **Network Traffic Analysis:**
    - Automatic baseline learning for normal network traffic patterns using cloud-native machine learning capabilities with automated alerting for significant deviations
    - Threat intelligence integration with commercial and government feeds for enhanced detection capabilities
    - Weekly security reviews and monthly executive summary reports including threat trends, incident summaries, and service performance metrics

- **Network Security Monitoring Operations:**
    - 24/7 network traffic monitoring and analysis
    - Network behavior analysis for detecting advanced persistent threats (APTs)
    - DNS monitoring and filtering for malicious domain detection
    - Integration with threat intelligence feeds for proactive threat detection

##### 3.2.2 Network Incident Response

- **Automated Network Response:**
    - Automated response capabilities for detected network threats
    - Network isolation and quarantine procedures for compromised systems
    - Traffic capture and analysis capabilities for incident investigation
    - Network forensics tools and procedures for security incident analysis
    - Coordination with security operations center (SOC) for incident response

#### 3.3 Intrusion Detection and Prevention Systems

Comprehensive intrusion detection and prevention capabilities shall protect against network-based attacks and unauthorized access attempts.

##### 3.3.1 Intrusion Detection and Prevention Implementation

- **Cloud-Native IDS/IPS Services:**
    - Cloud-native intrusion detection services shall be enabled with default threat detection rule sets and automatic threat intelligence updates
    - Network security groups and access control lists (NACLs) shall be configured to provide network-level intrusion prevention with default-deny policies
    - Web Application Firewall (WAF) services shall be deployed on internet-facing applications to detect and block common web attacks including SQL injection, XSS, and DDoS attempts

- **Automated Threat Response:**
    - Automated threat response capabilities shall include automatic IP blocking, traffic inspection escalation, and alert generation for security team review
    - DNS-based threat protection services shall block access to known malicious domains and command & control servers automatically
    - VPC Flow Logs and virtual network monitoring shall capture network traffic metadata for analysis with automated detection of suspicious patterns and geographic anomalies

- **IDS/IPS Management:**
    - Intrusion detection and prevention systems (IDS/IPS) with signature and anomaly-based detection
    - Regular updates of IDS/IPS signatures and threat detection rules
    - Tuning and optimization of IDS/IPS systems to minimize false positives
    - Integration with network security monitoring and incident response systems

#### 3.4 Firewall Management and Administration

Comprehensive firewall management shall provide perimeter protection and network access control across all network boundaries.

##### 3.4.1 Firewall Management Implementation

- **Firewall Architecture:**
    - Firewall deployment architecture shall provide defense-in-depth protection including perimeter firewalls, internal segmentation firewalls, web application firewalls, and cloud security groups
    - Network security zones shall be defined and implemented including Internet, DMZ, Internal, Management, and High-Security zones with zone-based access controls

- **Firewall Rule Management:**
    - Firewall rule development shall require business justification, security risk assessment, specific rule parameters, and documented purpose with expiration dates
    - Change management workflows shall require Security Officer approval for high-risk firewall rules with additional approvals for critical external access
    - Firewall logs shall be monitored continuously for security events including blocked connections, policy violations, and administrative access attempts
    - Quarterly firewall rule reviews shall identify unused or expired rules, overly permissive access, and opportunities for optimization and consolidation

#### 3.5 Network Access Control and Remote Access

Comprehensive network access controls shall ensure authorized access to network resources while preventing unauthorized access and maintaining security monitoring.

##### 3.5.1 Network Access Control Implementation

- **Network Access Control (NAC) Systems:**
    - Automated device discovery and classification for all devices connecting to corporate networks
    - Device compliance verification including security patch status, antivirus updates, and configuration compliance
    - Dynamic VLAN assignment based on device type, user role, and compliance status
    - Quarantine network for non-compliant devices with limited access and remediation capabilities
    - Integration with identity management systems for user-based access policies

##### 3.5.2 Remote Access Security

- **VPN and Remote Access Controls:**
    - Multi-factor authentication required for all remote access connections
    - End-to-end encryption for all remote access sessions using approved protocols
    - Remote access session monitoring and logging for security analysis
    - Time-limited remote access sessions with automatic disconnection
    - Device compliance verification for remote access endpoints

#### 3.6 Network Performance and Capacity Management

Network performance monitoring shall ensure adequate capacity and optimal performance while maintaining security monitoring capabilities.

##### 3.6.1 Network Performance Monitoring

- **Performance Monitoring Implementation:**
    - Real-time network performance monitoring including bandwidth utilization, latency, and packet loss
    - Capacity planning and forecasting based on historical usage patterns and business growth
    - Quality of Service (QoS) implementation to prioritize critical business traffic
    - Network optimization and traffic engineering to ensure optimal performance
    - Performance alerting and notification for capacity or performance issues

### 4. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 6. Responsibilities

|**Role**|**Responsibility**|
|---|---|
|**Network Security Manager**|Develop network security policies, oversee network security architecture, manage network security controls, and coordinate network security incident response.|
|**Network Engineers**|Design and maintain secure network architecture, implement network security controls, configure network devices, and monitor network security events.|
|**Security Operations Center (SOC)**|Monitor network security events 24/7, analyze network security alerts, coordinate network incident response, and provide network security monitoring.|
|**Information Security Officer**|Oversee network security program, approve network security policies, review network security assessments, and ensure regulatory compliance.|
|**Managed Security Service Provider (MSSP)**|Provide 24/7 network security monitoring, threat analysis, incident response capabilities, and network security expertise.|
|**System Administrators**|Configure network security settings on systems, implement network access controls, and maintain network security compliance.|
|**Firewall Administrators**|Configure and maintain firewall rules, monitor firewall logs, implement firewall changes, and ensure firewall compliance.|
|**Cloud Engineers**|Implement cloud network security controls, configure VPC security, manage cloud network services, and ensure cloud network compliance.|
|**All Engineering Staff**|Follow network security policies, implement network security controls in their areas, report network security issues, and participate in network security training.|
