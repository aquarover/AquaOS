# ENG-003 — Branch Strategy

| Field | Value |
|-------|-------|
| Document ID | ENG-003 |
| Version | 1.0.0 |
| Status | Approved |
| Owner | CTO |
| Reviewer | CTO |
| Approved By | CTO |
| Last Updated | 2026-08-11 |

---

# Purpose

This document defines how branches are created, named, used, and merged within Auqora Technologies.

The goal is to keep development organized while allowing multiple engineers to work safely in parallel.

---

# Primary Branch

## main

`main` is the stable and production-ready branch.

Rules:

- Direct commits are not allowed.
- Changes must come through a reviewed pull request.
- Only tested and approved changes may be merged.
- `main` should always remain deployable.

---

# Development Branches

### Feature

Used for new functionality.

```text
feature/<short-description>
Fix Branch

Used for correcting bugs or unexpected behavior.

fix/<short-description>

Examples:

fix/camera-stream
fix/api-timeout
fix/detection-confidence
Documentation Branch

Used for documentation-only changes.

docs/<short-description>

Examples:

docs/eng-003-branch-strategy
docs/api-documentation
docs/ai-pipeline
Hotfix Branch

Used for urgent fixes that require immediate attention.

hotfix/<short-description>

Examples:

hotfix/critical-api-error
hotfix/jetson-communication

Hotfixes must still be reviewed and tested before being merged into main.

Branch Lifecycle
main
  │
  ▼
Create Branch
  │
  ▼
Develop
  │
  ▼
Test
  │
  ▼
Commit
  │
  ▼
Push
  │
  ▼
Pull Request
  │
  ▼
Code Review
  │
  ▼
Approval
  │
  ▼
Merge
  │
  ▼
main
Branch Naming Rules

All branch names must:

Use lowercase letters.
Use hyphens to separate words.
Be short and descriptive.
Avoid spaces.
Avoid personal names.
Clearly communicate the purpose of the branch.
Good Examples
feature/plastic-detection
feature/mission-dashboard
fix/motor-control
fix/api-timeout
docs/ai-architecture
hotfix/critical-error
Avoid
DhanushBranch
new stuff
test123
my-feature
final-final-version
Branch Responsibility

The engineer creating a branch is responsible for:

Keeping the branch focused on one task.
Writing meaningful commits.
Testing changes before requesting review.
Keeping the branch reasonably up to date.
Resolving merge conflicts.
Providing a clear Pull Request description.
Updating relevant documentation when required.
Pull Request Rules

Every branch intended to be merged into main must be submitted through a Pull Request.

The Pull Request should clearly describe:

What was changed.
Why the change was made.
How the change was tested.
Any known limitations or issues.

At least one team member must review the Pull Request before merging.

For major architectural or security-related changes, CTO review is required.

Merge Rules

A branch may be merged only when:

The implementation is complete.
Required tests pass.
Documentation is updated when necessary.
The Pull Request has been reviewed.
Required approvals have been obtained.
No unresolved merge conflicts remain.

After successful merging, the branch may be deleted if it is no longer required.

Emergency Changes

Critical production issues may require a hotfix branch.

Example:

hotfix/critical-api-error

The engineer must:

Create the hotfix branch from main.
Implement the minimum required fix.
Test the fix.
Create a Pull Request.
Obtain the required review.
Merge the fix into main.
Document the issue and resolution when necessary.
Branch Protection

The main branch must be protected against accidental or unauthorized changes.

Protection should include:

Pull Request requirement.
Review requirement.
Status checks where applicable.
Prevention of direct pushes.
Prevention of force pushes.

Repository administrators may modify branch protection settings when necessary.

Version History
Version	Date	Changes
1.0.0	2026-08-11	Initial Branch Strategy