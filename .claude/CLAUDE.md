# Security Policies Git Workflow - STRICTLY ENFORCED

This project follows the Coral AI Git & GitHub Workflow Guide.
ALL git operations MUST comply with these rules.

## CRITICAL: Manual Approval Required

**Any deviation from these rules requires EXPLICIT manual approval from the user.**
Do NOT assume approval. Do NOT proceed without confirmation.
If a commit message, branch name, or PR title doesn't match the required format,
STOP and ask the user for the correct ticket ID or approval to deviate.

---

## Commit Message Format (REQUIRED)

**Pattern**: `[COR-XXX] Brief description`

**Validation Regex**: `^\[[Cc][Oo][Rr]-\d+(\s*,\s*[Cc][Oo][Rr]-\d+)*\]\s*.+`

### Examples

| Valid | Invalid |
|-------|---------|
| `[COR-123] Add access control policy` | `Add access policy` (missing ticket) |
| `[cor-123] Update compliance docs` | `COR-123 Update docs` (missing brackets) |
| `[COR-123, COR-456] Revise security SOPs` | `[COR123] Fix` (missing hyphen) |

### Rules

- Ticket ID is **required** in square brackets
- Case-insensitive: `COR`, `cor`, `Cor` all valid
- Multiple tickets allowed: `[COR-123, COR-456]`
- If no ticket ID provided, **ASK the user** - do NOT proceed without it

---

## Branch Naming Convention (REQUIRED)

**Pattern**: `COR-<ticket-number>-short-description`

### Examples

| Valid | Invalid |
|-------|---------|
| `COR-123-add-hipaa-policy` | `feature/hipaa-policy` (missing ticket) |
| `COR-456-update-soc2-controls` | `cor123-feature` (missing hyphen) |

---

## PR Title Format (REQUIRED)

### For PRs to `develop`:

**Pattern**: `[COR-XXX] Brief description`

### For PRs to `main` (releases):

Documentation projects typically don't have standalone releases.
If releasing, use infrastructure format: `cycle-<sprint>-release-infra-<number>`

---

## Merge Strategy

- **Feature branches**: Use `git rebase origin/develop` (NOT merge)
- **Releases to main**: Use merge commit (NOT squash/rebase)
- **NEVER** use the GitHub "Update branch" button

---

## Before Creating Commits

1. Verify you have a valid COR-XXX ticket ID
2. If no ticket ID is provided, **ASK the user for one**
3. Validate the commit message matches the required pattern
4. Do NOT proceed with commits that don't match the format

## Before Creating PRs

1. Verify the PR title matches the required format
2. Include the PR template sections (Description, Testing, Related Issues)

---

## Enforcement

Claude Code will:
- **REFUSE** commits without valid `[COR-XXX]` format
- **REFUSE** branches without valid `COR-XXX-` prefix
- **REFUSE** PRs without valid title format
- **ASK** for ticket ID if not provided
- **ASK** for explicit approval before any deviation

**No exceptions without explicit user approval.**
