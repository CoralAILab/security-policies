---
title: ePHI De-identification Policy (SEC-POL-014)
parent: Security Policies
nav_order: 14
---

### 1. Objective

The objective of this policy is to establish requirements for de-identifying electronic Protected Health Information (ePHI) using the HIPAA Safe Harbor method to enable internal testing, development, and analytics activities while ensuring regulatory compliance and protecting patient privacy.

### 2. Scope

This policy applies to all **ASM One Inc.** workforce members who de-identify ePHI for internal use in:

- Testing and development environments
- Analytics and reporting activities

This policy covers the de-identification process and resulting de-identified datasets. It does not apply to:

- External data sharing or third-party access (covered by Business Associate Agreements)
- Direct patient care or clinical operations
- Data that was never ePHI

### 3. Policy

**ASM One Inc.** shall implement de-identification controls that protect patient privacy while enabling internal business operations.

#### 3.1 De-Identification Method

All ePHI de-identification shall use the HIPAA Safe Harbor method as specified in 45 CFR § 164.514(b)(2).

- **ASM One Inc.** uses the Safe Harbor method exclusively; Expert Determination is not used.
- All 18 specified identifiers must be removed or generalized as described in Section 3.2.
- The person performing de-identification must meet the "no actual knowledge" standard as defined in Section 3.4.

Once properly de-identified under the Safe Harbor method, data is no longer considered ePHI or PHI under HIPAA and may be used without the restrictions that apply to protected health information.

##### 3.1.1 Training and Competency Requirements

Personnel who perform de-identification activities must:

- Complete de-identification training before performing any de-identification work. Training shall cover HIPAA Safe Harbor requirements, this policy, and the use of approved de-identification tools.
- Demonstrate competency through successful completion of a practical assessment.
- Complete annual refresher training to maintain authorization to perform de-identification.

The Privacy Officer shall maintain a list of personnel authorized to perform de-identification activities.

#### 3.2 Data Source Requirements

##### 3.2.1 Synthetic Data Requirement for Testing and Development

**Synthetic data shall be used for all testing and development purposes.** Real de-identified ePHI shall not be used in testing or development environments unless:

1. A documented business justification explains why synthetic data cannot meet the requirement.
2. The Privacy Officer approves the exception in writing.
3. The exception is reviewed and renewed every 90 days.

Approved exceptions shall be documented in the de-identification log with the business justification and Privacy Officer approval.

##### 3.2.2 De-identified Data for Analytics

Real de-identified ePHI may be used for analytics and reporting purposes when synthetic data cannot provide the statistical validity required. Such use must comply with all requirements of this policy, including statistical disclosure controls (Section 3.3).

#### 3.3 Identifier Removal Requirements

The following 18 identifiers must be removed or generalized from all de-identified datasets:

| # | Identifier | Removal Method |
|---|------------|----------------|
| 1 | Names | Remove completely |
| 2 | Geographic data smaller than state | Generalize to state level; if population <20,000, use "000" for zip code |
| 3 | Dates (except year) related to individual | Generalize to year only; ages 89+ report as "90+" |
| 4 | Phone numbers | Remove completely |
| 5 | Fax numbers | Remove completely |
| 6 | Email addresses | Remove completely |
| 7 | Social Security numbers | Remove completely |
| 8 | Medical record numbers | Remove completely |
| 9 | Health plan beneficiary numbers | Remove completely |
| 10 | Account numbers | Remove completely |
| 11 | Certificate/license numbers | Remove completely |
| 12 | Vehicle identifiers and serial numbers | Remove completely |
| 13 | Device identifiers and serial numbers | Remove completely |
| 14 | Web URLs | Remove completely |
| 15 | IP addresses | Remove completely |
| 16 | Biometric identifiers | Remove completely |
| 17 | Full-face photographs and comparable images | Remove completely |
| 18 | Any other unique identifying number, characteristic, or code | Remove completely |

**Implementation Requirements:**

- Automated de-identification tools shall be used. Manual de-identification is not permitted except with Privacy Officer approval for exceptional circumstances.
- Free-text fields (e.g., clinical notes) shall be processed using automated NLP-based scanning to detect and remove identifiers, followed by human review of flagged items.

#### 3.4 Statistical Disclosure Controls

De-identified datasets used for analytics shall implement the following controls to prevent inference-based re-identification:

##### 3.4.1 Minimum Cell Size

- Any aggregation, count, or statistical output must have a minimum cell size of **5 individuals**.
- Cells with fewer than 5 individuals shall be suppressed (not displayed) or combined with other cells.
- When suppression creates complementary disclosure (where suppressed values can be calculated from other cells), secondary suppression shall be applied.

##### 3.4.2 Rare Condition Protection

- Combinations of quasi-identifiers (e.g., rare disease + small geographic area + age range) that could identify individuals shall be generalized or suppressed.
- The Privacy Officer may require additional protections for datasets containing rare conditions, rare demographics, or small populations.

#### 3.5 Validation, Attestation, and Independent Review

Before any de-identified dataset is used, the following steps shall be completed:

##### 3.5.1 Technical Validation

The person performing de-identification shall verify that:
- All 18 identifier categories have been addressed using the removal methods specified in Section 3.3.
- Statistical disclosure controls (Section 3.4) have been applied for analytics datasets.
- Automated scanning has been completed for free-text fields.

##### 3.5.2 No Actual Knowledge Attestation

The person performing de-identification must attest that they have "no actual knowledge" that remaining information could identify an individual.

**"No Actual Knowledge" means:**

- The person has not viewed the source ePHI in its identified form for the same dataset.
- The person is not aware of any remaining data element that, alone or in combination with other reasonably available information, could identify a specific individual.
- The person has performed reasonable due diligence to identify potential re-identification risks.

**Documentation of No Actual Knowledge:**

The attestation shall include:
- A statement confirming the person did not have access to identified source data.
- Confirmation that due diligence was performed (e.g., review of quasi-identifier combinations, rare value analysis).
- Any concerns or limitations noted during the de-identification process.

If the person performing de-identification has viewed the source ePHI in identified form, a different qualified person must complete the attestation after independent review.

##### 3.5.3 Independent Quality Review

**Separation of Duties:** The person who performs de-identification shall not be the sole validator of their own work.

- **For all de-identification activities:** A second authorized person shall review a sample of the de-identified output to verify identifier removal and statistical controls.
- **Sample size:** At minimum, 5% of records or 100 records, whichever is smaller.
- **Review documentation:** The reviewer shall document their review, including sample size, any issues found, and confirmation of compliance.

If the independent review identifies issues, the dataset shall not be released until issues are remediated and the review is repeated.

##### 3.5.4 Documentation Requirements

Record the following for each de-identification activity:

| Field | Description |
|-------|-------------|
| Date of de-identification | When the de-identification was performed |
| Source dataset description | Description of the ePHI source (without including ePHI) |
| Destination use case | Testing, development, or analytics |
| Person performing de-identification | Name and confirmation of training completion |
| De-identification method | Tools used, configuration applied |
| Attestation confirmation | Signed no-knowledge attestation |
| Independent reviewer | Name of person who performed QA review |
| Review results | Sample size, issues found, resolution |
| Approval | Privacy Officer approval (if exception applies) |

Documentation shall be retained for the same period as the de-identified dataset or 6 years, whichever is longer, in accordance with HIPAA retention requirements.

#### 3.6 Permitted Uses

De-identified data under this policy may only be used for:

- **Testing and Development**: System testing, quality assurance activities, and developer environments (subject to synthetic data requirement in Section 3.2.1)
- **Analytics and Reporting**: Internal business analytics, operational reporting, and quality metrics

De-identified data shall not be:

- Shared with external parties without a separate data use agreement and Privacy Officer approval
- Subject to attempts at re-identification
- Combined with other datasets in ways that could enable re-identification

**Re-identification Prohibition**: **ASM One Inc.** does not maintain keys or mappings that would allow de-identified data to be linked back to individuals. Re-identification is prohibited.

#### 3.7 De-identification Failure Response

If ePHI is discovered in a dataset that was believed to be de-identified, the following steps shall be taken immediately:

##### 3.7.1 Immediate Actions

1. **Stop use**: Immediately cease all use of the affected dataset.
2. **Isolate**: Quarantine all copies of the affected dataset.
3. **Notify**: Report to the Privacy Officer within 4 hours of discovery.

##### 3.7.2 Assessment

The Privacy Officer shall:

1. Determine the scope of the failure (which identifiers were present, how many records affected).
2. Identify all locations where the dataset was used or stored.
3. Determine whether any unauthorized access or disclosure occurred.
4. Assess whether the incident constitutes a HIPAA breach requiring notification.

##### 3.7.3 Remediation

1. Properly de-identify or destroy all copies of the affected dataset.
2. Conduct root cause analysis to determine why the failure occurred.
3. Implement corrective actions to prevent recurrence.
4. Document the incident, findings, and corrective actions.

##### 3.7.4 Breach Determination

If the Privacy Officer determines that the de-identification failure resulted in unauthorized access or disclosure of ePHI, the incident shall be escalated to the Incident Response process (RES-POL-001) for breach determination and potential notification requirements.

#### 3.8 Audit and Monitoring

##### 3.8.1 Periodic Audit

The Security Officer shall conduct an audit of de-identification practices at least annually. The audit shall include:

- Review of de-identification documentation for completeness and accuracy.
- Verification that personnel performing de-identification have current training.
- Sampling of de-identified datasets to verify compliance with identifier removal requirements.
- Review of any exceptions granted and their continued validity.
- Assessment of statistical disclosure control effectiveness.

##### 3.8.2 Dataset Sampling

During each audit cycle, the Security Officer shall select a random sample of de-identified datasets created since the last audit and verify:

- All 18 identifier categories were properly addressed.
- Statistical disclosure controls were applied (for analytics datasets).
- Independent review was completed.
- Documentation is complete and accurate.

Sample size: At minimum, 10% of datasets created during the audit period or 5 datasets, whichever is greater.

##### 3.8.3 Audit Findings

Audit findings shall be documented and reported to the Privacy Officer. Critical findings (e.g., identifiers found in de-identified data, missing independent reviews) shall be remediated within 30 days. The Privacy Officer shall report audit results to the Information Security Committee quarterly.

### 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1, 3.3 | HIPAA Privacy Rule | 45 CFR § 164.514(b)(2) - Safe Harbor De-identification Standard |
| 3.5 | HITRUST CSF v11.2.0 | 10.i - Protection of System Test Data |
| 3.3, 3.4 | HITRUST CSF v11.2.0 | 13.j - Data Minimization |
| 3.6 | HITRUST CSF v11.2.0 | 13.l - Retention and Disposal |
| 3.3 | HITRUST CSF v11.2.0 | 06.d - Data Protection and Privacy of Covered Information |
| 3.5 | SOC 2 Trust Services Criteria | CC6.7 - Restriction and Protection of Information in Transmission and Processing |
| 3.7 | HIPAA Breach Notification Rule | 45 CFR § 164.400-414 |
| 3.8 | HITRUST CSF v11.2.0 | 06.g - Compliance with Security Policies and Standards |

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md) for standard terms.

Policy-specific definitions:

- **De-identification**: The process of removing specified identifiers from ePHI such that the remaining information cannot reasonably identify an individual, as defined by HIPAA (45 CFR § 164.514).

- **Safe Harbor Method**: A de-identification standard specified in HIPAA that requires removal of 18 specified identifiers and no actual knowledge that remaining information could identify an individual.

- **De-identified Data**: Information that has been processed to remove identifiers in accordance with the Safe Harbor method and is no longer considered ePHI or PHI under HIPAA.

- **No Actual Knowledge**: A standard requiring that the person certifying de-identification is not aware of any information that could be used, alone or in combination with other reasonably available information, to identify an individual who is a subject of the data.

- **Synthetic Data**: Artificially generated data that mimics the statistical properties of real data but contains no actual patient information.

- **Quasi-identifier**: A data element that is not a direct identifier but could contribute to re-identification when combined with other information (e.g., age, gender, diagnosis, geographic region).

- **Cell Suppression**: The practice of not displaying statistical results when the underlying count is below a minimum threshold to prevent identification of individuals.

### 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Privacy Officer** | Provide policy oversight; maintain list of authorized de-identification personnel; approve exceptions to synthetic data requirement; approve external data sharing; assess de-identification failures for breach determination; review quarterly audit results. |
| **Security Officer** | Conduct annual audits of de-identification practices; perform dataset sampling; report findings to Privacy Officer; verify training compliance. |
| **Data Steward / Developer** | Complete required training; perform de-identification activities using approved tools; complete attestation; maintain documentation; report de-identification failures immediately. |
| **Independent Reviewer** | Perform quality review of de-identified datasets; verify identifier removal and statistical controls; document review findings; escalate issues found. |
| **All Workforce Members** | Report any concerns about data that may not have been properly de-identified to the Privacy Officer within 24 hours. Complete de-identification training before performing any de-identification work. |
