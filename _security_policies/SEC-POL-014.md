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
- The person performing de-identification must have no actual knowledge that remaining information could identify an individual.

Once properly de-identified under the Safe Harbor method, data is no longer considered ePHI or PHI under HIPAA and may be used without the restrictions that apply to protected health information.

#### 3.2 Identifier Removal Requirements

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

**Implementation Guidance:**

- For testing and development purposes, synthetic data generation is preferred over de-identification when feasible.
- When de-identification is required, automated tools should be used where available to ensure consistency and completeness.
- Free-text fields (e.g., clinical notes) require careful review as they may contain identifiers embedded in narrative text.

#### 3.3 Validation and Attestation

Before any de-identified dataset is used, the following steps shall be completed:

1. **Technical Validation**: Verify that all 18 identifier categories have been addressed using the removal methods specified in Section 3.2.

2. **No-Knowledge Attestation**: The person performing de-identification must attest that they have no actual knowledge that the remaining information could be used alone or in combination with other information to identify any individual who is a subject of the information.

3. **Documentation**: Record the following for each de-identification activity:
   - Date of de-identification
   - Source dataset description
   - Destination use case (testing, development, or analytics)
   - Person performing de-identification
   - Attestation confirmation

Documentation shall be retained for the same period as the de-identified dataset or 6 years, whichever is longer, in accordance with HIPAA retention requirements.

#### 3.4 Permitted Uses

De-identified data under this policy may only be used for:

- **Testing and Development**: System testing, quality assurance activities, and developer environments
- **Analytics and Reporting**: Internal business analytics, operational reporting, and quality metrics

De-identified data shall not be:

- Shared with external parties without a separate data use agreement and Privacy Officer approval
- Subject to attempts at re-identification
- Combined with other datasets in ways that could enable re-identification

**Re-identification Prohibition**: **ASM One Inc.** does not maintain keys or mappings that would allow de-identified data to be linked back to individuals. Re-identification is prohibited.

### 4. Standards Compliance

| **Policy Section** | **Standard/Framework** | **Control Reference** |
|---|---|---|
| 3.1, 3.2 | HIPAA Privacy Rule | 45 CFR § 164.514(b)(2) - Safe Harbor De-identification Standard |
| 3.3 | HITRUST CSF v11.2.0 | 10.i - Protection of System Test Data |
| 3.2 | HITRUST CSF v11.2.0 | 13.j - Data Minimization |
| 3.4 | HITRUST CSF v11.2.0 | 13.l - Retention and Disposal |
| 3.2 | HITRUST CSF v11.2.0 | 06.d - Data Protection and Privacy of Covered Information |
| 3.3 | SOC 2 Trust Services Criteria | CC6.7 - Restriction and Protection of Information in Transmission and Processing |

### 5. Definitions

See [Annex: Glossary](../_annexes/glossary.md) for standard terms.

Policy-specific definitions:

- **De-identification**: The process of removing specified identifiers from ePHI such that the remaining information cannot reasonably identify an individual, as defined by HIPAA (45 CFR § 164.514).

- **Safe Harbor Method**: A de-identification standard specified in HIPAA that requires removal of 18 specified identifiers and no actual knowledge that remaining information could identify an individual.

- **De-identified Data**: Information that has been processed to remove identifiers in accordance with the Safe Harbor method and is no longer considered ePHI or PHI under HIPAA.

### 6. Responsibilities

| **Role** | **Responsibility** |
|---|---|
| **Privacy Officer** | Provide policy oversight, validate de-identification practices through periodic review, and approve any exceptions or external data sharing requests. |
| **Data Steward / Developer** | Perform de-identification activities, complete required attestation, maintain documentation, and ensure compliance with identifier removal requirements. |
| **Security Officer** | Conduct periodic audits of de-identification practices and documentation to verify compliance with this policy. |
| **All Workforce Members** | Report any concerns about data that may not have been properly de-identified to the Privacy Officer. |
