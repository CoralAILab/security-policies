---
title: Business Continuity Management Policy (RES-POL-002)
parent: Resilience Policies
nav_order: 2
---
### 1. Objective

The objective of this policy is to establish a comprehensive business continuity management framework for **ASM One Inc.** that ensures the continuation of critical business operations and essential services during disruptions. This policy focuses on business process continuity, stakeholder communication, alternative operating procedures, and organizational resilience while technical disaster recovery capabilities are addressed in the Disaster Recovery and Technical Operations Policy (RES-POL-005). By implementing structured business continuity capabilities including business impact analysis, emergency response procedures, and alternative operations, **ASM One Inc.** maintains essential service delivery to customers, protects electronic Protected Health Information (ePHI), meets regulatory obligations under HIPAA, HITECH, and SOC 2, and minimizes business impact during various types of disruptions.

### 2. Scope

This policy applies to all **ASM One Inc.** workforce members, business units, business processes, and third-party service providers that support critical business operations. It encompasses business continuity planning and response for all types of disruptions including natural disasters, pandemics, cyber incidents, supply chain disruptions, workforce shortages, and other events that could impact business operations. This policy covers business process continuity, stakeholder management, emergency communications, alternative work arrangements, and vendor continuity management, while technical system recovery is addressed through the Disaster Recovery and Technical Operations Policy (RES-POL-005).

### 3. Policy

**ASM One Inc.** shall maintain comprehensive business continuity management capabilities that enable the organization to continue critical business operations during disruptions through alternative procedures, emergency response coordination, and stakeholder management, with technical system recovery addressed through the Disaster Recovery and Technical Operations Policy (RES-POL-005).

#### 3.1 Business Continuity Framework

- **ASM One Inc.** shall implement a structured approach to business continuity management based on industry best practices and regulatory requirements.

##### 3.1.1 Business Continuity Principles

- **Workforce Safety Priority:**
    - The safety and security of workforce members shall be the highest priority in all emergency situations.
    - Emergency communication and safety procedures shall take precedence over business operations.
    - Clear communication channels and emergency coordination procedures shall be maintained at all times.

- **Essential Services Continuity:**
    - Critical business functions shall be identified and prioritized for continuity during disruptions.
    - Minimum service levels shall be defined for essential operations to ensure baseline service delivery.
    - Alternative methods and resources shall be available to maintain critical services during emergencies.
    - Customer-facing services and ePHI processing functions shall receive highest priority for resource allocation.

- **Regulatory Compliance:**
    - Business continuity plans shall ensure continued compliance with HIPAA, HITECH, and other applicable regulations.
    - ePHI availability and protection shall be maintained during disruptions according to regulatory requirements.
    - Audit trails and documentation requirements shall be met even during emergency operations.
    - Regulatory notification requirements shall be incorporated into emergency procedures.

- **Stakeholder Communication:**
    - Clear, timely, and accurate communication shall be maintained with all stakeholders throughout disruptions.
    - Multiple communication channels shall be available for redundancy to ensure reliable communications.
    - Regular updates shall be provided during extended disruptions to maintain stakeholder awareness.
    - Post-incident communication shall address lessons learned and improvements implemented.

##### 3.1.2 Business Impact Analysis (BIA)

The Business Continuity Manager, in coordination with Business Unit Leaders, shall conduct and formally document a comprehensive Business Impact Analysis (BIA) at least annually, or whenever a significant change to business operations occurs. The BIA report, which defines the recovery requirements for all critical functions, shall be reviewed and formally approved by the Information Security Committee.

- **Critical Function Identification:**
- **Immediate (0-4 hours):** Core document processing API, authentication and authorization systems, database infrastructure
- **Urgent (4-24 hours):** Customer portal, webhook delivery systems, reporting and analytics, notification services
- **Important (1-3 days):** Administrative systems, billing integration, customer support tools, internal collaboration tools
- **Deferrable (3+ days):** Development and staging environments, training systems, archival processes

- **Impact Assessment Criteria:**
- **Financial Impact:** Revenue loss, additional costs, regulatory fines, contractual penalties
- **Operational Impact:** Service disruption, productivity loss, customer dissatisfaction
- **Regulatory Impact:** Compliance violations, reporting failures, audit findings
- **Reputational Impact:** Public relations damage, loss of stakeholder confidence
- **Customer Impact:** Service availability to healthcare providers, downstream effects on customer operations

- **Recovery Time Objectives (RTO):**
    - Maximum acceptable downtime for each critical business function
    - Immediate: **1 hour** maximum downtime
    - Urgent: **4 hours** maximum downtime
    - Important: **24 hours** maximum downtime
    - Deferrable: **72 hours** maximum downtime

- **Recovery Point Objectives (RPO):**
    - Maximum acceptable data loss for each critical system
    - Critical ePHI systems: **15 minutes** maximum data loss
    - Financial systems: **1 hour** maximum data loss
    - Administrative systems: **4 hours** maximum data loss
    - Development systems: **24 hours** maximum data loss

#### 3.2 Technical Disaster Recovery Integration

All technical disaster recovery planning, data backup and recovery systems, IT infrastructure recovery, and system restoration procedures shall be implemented as defined in the Disaster Recovery and Technical Operations Policy (RES-POL-005). This includes comprehensive IT disaster recovery strategy, backup systems management, system recovery procedures, and technical performance monitoring that supports the business continuity requirements defined in this policy.

#### 3.3 Emergency Response Procedures

Standardized emergency response procedures shall guide initial response actions during various types of disruptions.

##### 3.3.1 Emergency Activation Procedures

- **Incident Assessment:**
    - Initial situation assessment and impact determination
    - Activation of appropriate emergency response level
    - Notification of emergency response team members
    - Establishment of virtual emergency operations coordination
    - Communication with key stakeholders and authorities

- **Emergency Response Levels:**
- **Level 1 - Service Disruption:** Single service or limited impact requiring immediate response
- **Level 2 - Major Incident:** Multiple services or significant customer impact requiring coordinated response
- **Level 3 - Enterprise Emergency:** Organization-wide impact requiring full emergency response activation

##### 3.3.2 Communication Procedures

- **Emergency Notification System:**
    - Automated notification system for workforce members
    - Multiple communication channels (phone, email, text, Slack)
    - 24/7 emergency communication capabilities
    - Customer status page and notification updates
    - Integration with incident management systems

- **Stakeholder Communication:**
    - Immediate notification of executive leadership
    - Regular updates to workforce members
    - Communication with customers and business partners
    - Coordination with regulatory agencies if required
    - External communication management for significant incidents

#### 3.4 Alternative Operations

Alternative operating procedures shall enable continuation of critical business functions during disruptions.

##### 3.4.1 Remote Work Continuity

As a fully remote organization, **ASM One Inc.** maintains inherent resilience through distributed workforce operations:

- **Distributed Workforce:**
    - Geographic distribution of workforce reduces single-point-of-failure risks
    - Workforce members equipped for full productivity from any location
    - Cloud-based tools enable seamless collaboration regardless of individual circumstances
    - Redundant communication channels for team coordination

- **Infrastructure Redundancy:**
    - Cloud infrastructure with multi-region capabilities
    - Multiple internet connectivity options for critical personnel
    - Backup communication systems (phone, alternate messaging platforms)
    - Secure remote access maintained for all workforce members

##### 3.4.2 Critical System Alternatives

- **Manual Procedures:**
    - Documented manual procedures for critical electronic systems where feasible
    - Alternative communication methods (phone, alternate platforms)
    - Emergency customer communication procedures
    - Escalation procedures for extended outages

- **Vendor Support Services:**
    - Emergency vendor agreements for rapid response
    - 24/7 vendor support for critical systems and infrastructure
    - Expedited procurement procedures for emergency equipment
    - Alternative vendor options for single points of failure
    - Service level agreements with guaranteed emergency response times

#### 3.5 Testing and Maintenance

Regular testing and maintenance shall ensure the effectiveness of business continuity and disaster recovery capabilities.

##### 3.5.1 Testing Schedule and Requirements

- **Monthly Testing:**
    - Backup and recovery procedures for critical systems
    - Emergency communication systems and notification procedures
    - Vendor emergency response capabilities
    - Documentation updates and contact information verification

- **Quarterly Testing:**
    - Tabletop exercises for emergency response scenarios
    - Partial system recovery testing and validation
    - Workforce training and awareness programs
    - Business impact analysis updates and revisions

- **Annual Testing:**
    - Full-scale business continuity exercise
    - Complete disaster recovery simulation
    - Comprehensive plan review and updates
    - Third-party assessment of continuity capabilities
    - Regulatory compliance validation and reporting

##### 3.5.2 Plan Maintenance and Updates

- **Regular Plan Updates:**
    - Annual comprehensive review and revision of all plans
    - Quarterly updates based on organizational changes
    - Monthly contact information and resource verification
    - Immediate updates following significant incidents or changes
    - Version control and distribution management for all plans

- **Training and Awareness:**
    - Annual business continuity training for all workforce members
    - Specialized training for emergency response team members
    - New employee orientation including emergency procedures
    - Regular drills and exercises to maintain readiness
    - Cross-training programs to reduce single points of failure

#### 3.6 Vendor and Third-Party Management

Business continuity requirements shall be incorporated into vendor management and third-party relationships.

##### 3.6.1 Vendor Continuity Requirements

- **Service Level Agreements:**
    - Specific business continuity and disaster recovery requirements
    - Guaranteed response times for emergency situations
    - Alternative service delivery methods during disruptions
    - Regular testing and validation of vendor continuity capabilities
    - Financial penalties for continuity failures and service level breaches

- **Vendor Assessment and Monitoring:**
    - Annual assessment of vendor business continuity capabilities
    - Regular review of vendor disaster recovery plans and procedures
    - Monitoring of vendor financial stability and business viability
    - Evaluation of vendor geographic risk factors and concentration
    - Validation of vendor backup and alternative service arrangements

##### 3.6.2 Business Associate Agreements

- **HIPAA Compliance Requirements:**
    - Business continuity provisions in all Business Associate Agreements
    - ePHI protection and availability requirements during emergencies
    - Breach notification procedures for continuity-related incidents
    - Audit and compliance requirements for emergency operations
    - Data backup and recovery requirements for ePHI systems

#### 3.7 Business Recovery and Restoration

Systematic business recovery procedures shall guide the restoration of normal business operations following emergency situations, with technical system recovery coordinated through RES-POL-005.

##### 3.7.1 Business Recovery Procedures

- **Operational Assessment:**
    - Comprehensive assessment of service capabilities and business operations
    - Business process and service capability evaluation and validation
    - Workforce accountability and availability assessment
    - Vendor and supply chain impact assessment and alternative sourcing

- **Phased Business Recovery Approach:**
    - **Phase 1**: Workforce safety confirmation and immediate emergency response coordination
    - **Phase 2**: Critical business process restoration and essential service resumption
    - **Phase 3**: Full operational capability restoration and normal service levels
    - **Phase 4**: Normal operations resumption and lessons learned integration
    - Business process dependencies mapping and coordinated restoration

##### 3.7.2 Post-Incident Review and Improvement

Following any activation of the business continuity plan, a formal post-incident review shall be conducted to ensure organizational learning and improvement.

- **Comprehensive Business Impact Analysis:**
    - Formal Post-Incident Report detailing business impact, response effectiveness, and operational lessons learned
    - Business process performance analysis and service level achievement assessment
    - Financial impact assessment and cost analysis of business disruption and response
    - Stakeholder feedback collection and satisfaction analysis
    - Regulatory compliance validation and business requirement fulfillment

- **Business Process Improvement Implementation:**
    - All business findings and lessons learned shall be documented and prioritized
    - Business improvement action items shall be assigned owners and due dates and tracked to completion
    - Business continuity plans and procedures shall be updated based on approved improvements
    - Business training programs and workforce development based on lessons learned
    - Vendor relationships and service agreements modifications and improvements
    - Integration of business process improvements with technical disaster recovery enhancements

## 4. Standards Compliance

See [Annex: Control Mapping](../_annexes/control_mapping.md)

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md)

### 6. Responsibilities

The following roles and responsibilities apply specifically to business continuity management functions, with technical disaster recovery responsibilities defined in RES-POL-005.

|**Role**|**Responsibility**|
|---|---|
|**Executive Leadership**|Provide strategic direction and resources for business continuity program, approve business operational plans and resource allocation, and communicate with external stakeholders during business emergencies.|
|**Business Continuity Manager**|Develop and maintain business continuity plans, coordinate business impact analysis and testing, manage business emergency response activities, and ensure business operational compliance.|
|**Business Unit Leaders**|Implement business unit specific continuity plans, coordinate business process restoration, manage departmental business communications, and support workforce business needs.|
|**Emergency Operations Team**|Coordinate business emergency response activities, manage emergency operations coordination for business functions, communicate with business stakeholders, and ensure workforce safety and business operations.|
|**Human Resources**|Manage workforce accountability and business communications, support workforce welfare during business disruptions, and maintain emergency contact information.|
|**Legal and Compliance**|Ensure regulatory compliance during business emergencies, manage legal implications of business incidents, coordinate with business authorities, and handle business insurance claims.|
|**Communications Team**|Manage external business communications, coordinate with customers, handle business crisis communications, and maintain business stakeholder relationships.|
|**All Workforce Members**|Follow business emergency procedures, participate in business continuity training and drills, report business safety concerns, and support business recovery efforts as assigned.|
