# ENG-002 — Git Workflow

| Field | Value |
|-------|-------|
| Document ID | ENG-002 |
| Version | 1.0.0 |
| Status | Approved |
| Owner | CTO |
| Reviewer | CTO |
| Approved By | CTO |
| Last Updated | 2026-08-03 |

---

# Purpose

This document defines the official Git workflow followed by the Aqua Rover Technologies engineering team to ensure consistent, traceable, and collaborative software development.

---

# Workflow

```text
Create Branch
      ↓
Develop
      ↓
Commit
      ↓
Push
      ↓
Review
      ↓
Merge
```

---

# Branch Naming

Feature

```text
feature/ai-detection
```

Bug Fix

```text
fix/dashboard-api
```

Documentation

```text
docs/git-workflow
```

---

# Commit Messages

Use Conventional Commits.

Examples:

```text
feat: add plastic detection module

fix: correct motor controller bug

docs: update Git workflow

refactor: improve API structure

chore: update dependencies
```

---

# Pull Request Checklist

Before requesting a review:

- Code compiles successfully.
- Documentation updated if required.
- Meaningful commit messages used.
- No unnecessary files included.

---

# Best Practices

- Commit small, meaningful changes.
- Push code regularly.
- Never force push to the main branch.
- Review code before merging.

---

# Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0.0 | 2026-08-03 | Initial Git Workflow |