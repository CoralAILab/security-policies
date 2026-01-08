# Security Procedure Automation Guide

This file contains automation instructions for Claude Code to execute security and compliance procedures.

**Location:** `/Users/seantodd/projects/coral/repos/security-policies/.claude/AUTOMATION.md`
**Purpose:** Centralized automation workflows for scheduled compliance activities
**Maintenance:** Update when procedures change or new procedures are automated

---

## Annual User Access Rights Review

**Frequency:** Annual (Q1 - January) or event-driven (major org changes)
**HITRUST Control:** 01.e (Access restriction)

### When to Run

**Trigger phrases:**
- "Run the annual access rights review"
- "Execute the annual access rights review"
- "Generate the user access rights report"

**Scheduled execution:** First week of January (Q1)

### Automation Flow

#### 1. Pre-Flight Checks
- Verify Azure CLI authentication: `az account show`
- Check permissions: `User.Read.All`, `Group.Read.All`, `RoleAssignment.Read.All`
- Create working directory: `/tmp/access-review-YYYY/`
- Verify jq installed: `which jq` (install via `brew install jq` if missing)

#### 2. Data Collection (Enhanced Azure CLI Queries)

Execute these queries in sequence:
- User accounts with `accountEnabled`, `userType`, `createdDateTime` fields
- Group memberships for each user (resolve IDs to group names)
- Service principals with metadata (description, tags, appId)
- Role assignments enriched with service principal display names
- Conditional Access policies for break-glass account detection

**Key workaround:** Azure AD Premium P1 required for `signInActivity` field. Use group membership + role assignment presence as activity proxy.

#### 3. Analysis (jq Processing)

Apply these analysis steps:
- Calculate risk scores (0-100 scale based on privilege, inactivity, account type)
- Detect Separation of Duties (SOD) violations
- Identify undocumented service principals
- Flag guest users without expiration dates
- Validate break-glass account security controls

#### 4. Report Generation

Generate 10-section markdown report:
1. Executive Summary (with high-risk findings count)
2. User Accounts (with risk scores and status)
3. Service Principals (categorized by pattern matching)
4. Group Memberships (per-user membership lists)
5. High-Privilege Roles (with business justifications)
6. Separation of Duties Analysis (conflict detection)
7. Guest/External Users (with expiration tracking)
8. Break-Glass Accounts (security validation)
9. Manager Attestation Workflow (Linear ticket generation)
10. Risk-Prioritized Recommended Actions

Output: `access-rights-report-YYYY-MM-DD.md`

#### 5. Ticket Creation (Linear)

Create structured ticket hierarchy:
- Master ticket: `[COR-XXXX] Annual Access Rights Review YYYY` (Project: Security Events, Team: Audits)
- Risk remediation tickets: `RISK-001`, `RISK-002`, etc. (one per finding)
- Manager attestation tickets (one per manager)

#### 6. Post-Review Activities

- Archive artifacts to `/security-policies/audits/access-review-YYYY/`
- CISO review and signature
- Update access control matrix document
- Schedule remediation verification (per risk SLA)

### Execution Command

```zsh
cd /tmp/access-review-YYYY
./generate-enhanced-report.zsh
```

### Output Artifacts

| Artifact | Purpose |
|----------|---------|
| `access-rights-report-YYYY-MM-DD.md` | Primary review document |
| `azure-ad-users-enhanced.json` | User account data with status |
| `azure-service-principals.json` | Service principal inventory |
| `azure-role-assignments-enriched.json` | RBAC assignments with context |
| `user-groups.jsonl` | Per-user group memberships |
| `break-glass-accounts.json` | Emergency access account list |
| `attestations/manager-[name].md` | Manager attestation forms |

### Known Limitations

| Limitation | Workaround |
|------------|------------|
| Sign-in activity unavailable (requires Azure AD Premium P1) | Use group membership + role assignments as activity proxy |
| Service principal context gaps | Categorize by pattern matching (Defender, AKS, identity.azure.net patterns) |
| Manual manager attestations required | Generate Linear tickets with attestation forms attached |

### Success Criteria Checklist

- [ ] All 10 report sections generated with accurate data
- [ ] Risk scores calculated for all users (0-100 scale)
- [ ] Service principals categorized (with documentation gap identification)
- [ ] SOD violations identified and documented
- [ ] Break-glass accounts validated against CA policies
- [ ] CISO review completed and approval documented
- [ ] Remediation tickets created for all findings

### Related Documents

- Script: `/tmp/access-review-YYYY/generate-enhanced-report.zsh`
- jq filters: `/tmp/access-review-YYYY/jq-filters/`
- Automation guide: `/Users/seantodd/projects/coral/repos/security-policies/.claude/AUTOMATION.md`

---

## Future Procedures

Add automation instructions for other security procedures here:
- SEC-PROC-016: FleetDM Monthly Compliance Report
- SEC-PROC-017: Quarterly Device Audit
- ENG-PROC-001: Monthly Vulnerability Scan
- etc.
