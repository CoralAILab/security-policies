---
title: Schedule of Security Procedures (ISMS-SUP-001)
parent: ISMS Supplements
nav_order: 1
---

#### **Monthly Procedures**

These procedures shall be conducted and documented every month to ensure continuous security monitoring and threat awareness.

| **Procedure (Code)**                                                 | **Primary Owner**        | **Description**                                                                                                                    | **HITRUST Control** |
| -------------------------------------------------------------------- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| **Security Monitoring Review Procedure** (SEC-PROC-010)              | Security Team            | Monthly review of security monitoring alerts, SIEM events, and anomaly detection reports to identify patterns and emerging threats. | 09.ab               |
| **Vulnerability Management Review Procedure** (SEC-PROC-015)         | Security Team            | Monthly review of vulnerability scanning results, remediation progress, and SLA compliance to verify the continuous vulnerability management process is effective. | 10.m                |
| **SAST Results Review Procedure** (ENG-PROC-001-A)                   | Security Team            | Monthly review of static application security testing (SAST) findings from CI/CD pipelines, including false positive triaging and remediation tracking. | 10.m                |
| **Backup Verification Review Procedure** (OP-PROC-009)               | IT Department            | Monthly verification that backup jobs completed successfully, restore testing samples are valid, and backup integrity is maintained. | 09.l                |
| **Automated Privileged Access Validation** (ENG-PROC-006-A)          | Security Team            | Monthly automated validation of privileged access via monitoring tools, verifying that privileged account usage aligns with approved access and detecting anomalies. | 01.c, 01.e          |
| **Endpoint Compliance Report Procedure** (SEC-PROC-016)              | Security Team            | Monthly FleetDM compliance report showing device encryption, firewall, baseline, and AV compliance rates with threshold-based remediation ticketing. | 10.a, 09.ab         |

#### **Quarterly Procedures**

These procedures shall be conducted and documented every three months to ensure ongoing compliance and security posture management.

| **Procedure (Code)**                                                 | **Primary Owner**        | **Description**                                                                                                                    | **HITRUST Control** |
| -------------------------------------------------------------------- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| **Privileged Infrastructure Access Review Procedure** (ENG-PROC-006-B) | Security Team            | Quarterly manual review and certification of all user accounts with privileged access, including documentation of access justification and manager approval. | 01.c, 01.e          |
| **Incident Trend Analysis Procedure** (SEC-PROC-011)                 | Security Team            | Quarterly review of incident patterns, lessons learned aggregation, and security trend analysis to improve incident response.      | 11.d                |
| **DAST Results Review Procedure** (ENG-PROC-001-B)                   | Security Team            | Quarterly review of dynamic application security testing (DAST) findings from deployment pipelines, including remediation status and pre-production gate enforcement. | 10.m                |
| **Configuration Baseline Review Procedure** (ENG-PROC-008)           | Security Team            | Quarterly review of system configurations against security baselines to detect drift and ensure hardening standards are maintained. | 06.h                |
| **BCDR Tabletop Exercise** (RES-PROC-007-A)                          | Business Continuity Manager | Quarterly tabletop exercise to walk through disaster recovery and business continuity scenarios, testing decision-making and communication procedures. | 12.e                |
| **Device Baseline Audit Procedure** (SEC-PROC-017)                   | Security Team            | Quarterly comprehensive audit of all FleetDM policies with HITRUST evidence generation, baseline drift detection, and device-level remediation ticketing. | 06.h, 10.a          |

#### **Semi-Annual Procedures**

These procedures shall be performed twice per year to ensure ongoing vendor risk management and third-party security compliance.

| **Procedure (Code)**                                                 | **Primary Owner**        | **Description**                                                                                                                    | **HITRUST Control** |
| -------------------------------------------------------------------- | ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| **Existing Vendor Risk Reassessment Procedure** (SEC-PROC-014)       | Security Team            | Semi-annual reassessment of existing high-risk vendors' security posture, including review of SOC 2 reports and BAA compliance.    | 05.i, 05.k, 09.f    |

#### **Annual Procedures**

These procedures shall be performed at least once per year to satisfy major compliance, assessment, and testing mandates.

| **Procedure (Code)**                                               | **Primary Owner**           | **Description**                                                                                                                              | **HITRUST Control** |
| ------------------------------------------------------------------ | --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- |
| **Information Security Committee Charter Procedure** (SEC-PROC-001) | Committee Chair            | Defines the operating rules and responsibilities of the Information Security Committee; the charter shall be reviewed annually.              | 00.a, 05.a          |
| **Internal Audit Procedure** (SEC-PROC-002)                        | Head of Internal Audit      | Outlines the process for planning, conducting, and reporting on annual internal audits of the Information Security Management System.        | 06.i                |
| **Risk Assessment Procedure** (SEC-PROC-004)                       | Security Officer            | Establishes a systematic process for conducting risk assessments annually and on an ad-hoc basis when significant changes occur.             | 03.b                |
| **Incident Response Plan (IRP)** ([RES-PROC-001])                  | Security Team               | Provides actionable steps for responding to incidents, including conducting annual training and simulation exercises.                        | 11.c                |
| **Business Impact Analysis (BIA) Procedure** ([RES-PROC-004])      | Business Continuity Manager | Defines the methodology for conducting the annual Business Impact Analysis to identify critical functions and establish recovery objectives. | 12.b                |
| **Full DR Simulation and Recovery Test** ([RES-PROC-007-B])        | Business Continuity Manager | Annual full-scale disaster recovery simulation including technical system recovery, data restoration verification, and RTO/RPO validation. Tabletop exercises are conducted quarterly per RES-PROC-007-A. | 12.e                |
| **Penetration Testing Procedure** (ENG-PROC-001-C)                 | Security Team               | Annual penetration testing by qualified security professionals for applications handling sensitive data. SAST/DAST reviews are conducted monthly/quarterly per ENG-PROC-001-A and ENG-PROC-001-B. | 10.m                |
| **Facility Access Management Procedure** (SEC-PROC-006)            | Facilities/Security Team    | Describes the process for managing physical facility access, including conducting and documenting annual access reviews.                     | 08.b                |
| **User Access Rights Review Procedure** (AC-PROC-005)              | IT Department               | Annual review of ALL user access rights across systems, verifying least privilege and appropriate access levels.                             | 01.e                |
| **Security Awareness Training Verification** (HR-PROC-001)         | Human Resources             | Annual verification that all workforce members have completed required security and privacy awareness training.                              | 02.e                |
| **Information Security Policy Review Procedure** (SEC-PROC-012)    | Security Officer            | Annual comprehensive review and update of the Information Security Policy to ensure alignment with current threats and regulations.          | 04.b                |
| **Independent Security Review Procedure** (SEC-PROC-013)           | External Auditor            | Annual independent review of information security program by a qualified third party to ensure objective assessment.                         | 05.h                |
| **Technical Compliance Review Procedure** (ENG-PROC-007)           | Security Team               | Annual review of technical compliance with security configurations, baselines, and hardening standards.                                      | 06.h                |

#### **Ad-Hoc / As-Needed / Event-Driven Procedures**

These procedures are not performed on a fixed schedule but are triggered by specific events such as a new hire, a security incident, or a request for a new system.

| **Procedure (Code)**                                                            | **Primary Owner**            | **Description**                                                                                                                         |
| ------------------------------------------------------------------------------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Password Policy Exception Procedure** (SEC-PROC-003)                          | Security Officer             | Provides a formal process for requesting, reviewing, and documenting exceptions to the Password Policy.                                 |
| **Vendor Risk Assessment and Onboarding Procedure** (SEC-PROC-005)              | Security Team                | Details the process for assessing a new vendor's security posture before engagement.                                                    |
| **AI Tool Risk Assessment and Approval Procedure** (SEC-PROC-007)               | AI Governance Committee      | Defines the process for performing a risk assessment on new AI tools before they are approved for use.                                  |
| **Vulnerability Management Procedure** (SEC-PROC-008)                           | Security Team                | Describes the continuous workflow for identifying, prioritizing, remediating, and verifying system vulnerabilities.                     |
| **Vulnerability Management Exception Procedure** (SEC-PROC-009)                 | Security Officer             | Outlines the process for formally requesting and documenting an exception to a vulnerability remediation Service Level Agreement (SLA). |
| **Acceptable Use Policy Violation Investigation Procedure** (AC-PROC-001)       | Security Officer             | Defines the process for investigating and responding to reported violations of the acceptable use policy.                               |
| **Bring Your Own Device (BYOD) Onboarding Procedure** (AC-PROC-002)             | IT Department                | Establishes the process for registering and securing a personally-owned device for access to company resources.                         |
| **Access Control Management Procedure** (AC-PROC-004)                           | IT Department                | Defines the process for managing the lifecycle of user access, including provisioning, modification, and revocation.                    |
| **HIPAA Breach Risk Assessment Procedure** ([RES-PROC-002])                     | Privacy Officer              | Guides the formal risk assessment required to determine if an incident qualifies as a notifiable HIPAA breach.                          |
| **Post-Incident Review Procedure** ([RES-PROC-003])                             | Incident Commander           | Outlines the process for conducting a formal 'lessons learned' review after a significant incident is resolved.                         |
| **IT Disaster Recovery Plan (DRP)** ([RES-PROC-005])                            | BCDR Steering Committee      | Provides technical procedures for recovering IT infrastructure in the event of a declared disaster.                                     |
| **Business Continuity Plan (BCP)** ([RES-PROC-006])                             | BCDR Steering Committee      | Outlines procedures for activating emergency response and continuing critical business functions during a disruption.                   |
| **Mobile Device Onboarding and Security Configuration Procedure** (OP-PROC-002) | IT Security Team             | Details the steps for enrolling a mobile device in the MDM system and ensuring it meets security requirements.                          |
| **Lost or Stolen Mobile Device Response Procedure** (OP-PROC-003)               | IT Security Team             | Provides the immediate steps to take when a mobile device used for company business is reported lost or stolen.                         |
| **Secure Media Disposal and Sanitization Procedure** (OP-PROC-004)              | IT Team                      | Provides instructions for securely destroying or sanitizing media that is at the end of its lifecycle.                                  |
| **Legal Hold Procedure** (OP-PROC-005)                                          | Legal Team                   | Outlines the steps for issuing, tracking, and releasing a legal hold on information relevant to legal matters.                          |
| **Workforce Screening and Background Check Procedure** (OP-PROC-006)            | Human Resources (HR)         | Outlines the formal process for conducting required background checks on all candidates for employment.                                 |
| **Employee Onboarding and Offboarding Security Procedure** (OP-PROC-007)        | Human Resources (HR)         | Provides a formal checklist to ensure all security tasks are completed during employee onboarding and termination.                      |
| **Security Policy Sanction Procedure** (OP-PROC-008)                            | Manager & HR                 | Describes the process for documenting security policy violations and applying appropriate disciplinary actions.                         |
| **Third-Party Component Security Review Procedure** (ENG-PROC-002)              | Development Team Lead        | Defines the steps for reviewing and approving the use of new third-party software components.                                           |
| **Standard Change Management Procedure** (ENG-PROC-003)                         | Engineering Lead             | Details the process for managing a standard, non-emergency change to a production application or configuration.                         |
| **Emergency Change Management Procedure** (ENG-PROC-004)                        | Engineering & Security Teams | Outlines the expedited process for authorizing and deploying an emergency change to resolve a critical issue.                           |
