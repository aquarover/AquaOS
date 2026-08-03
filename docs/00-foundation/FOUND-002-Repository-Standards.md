# FOUND-002 — Repository Standards

| Field | Value |
|-------|-------|
| Document ID | FOUND-002 |
| Version | 1.0.0 |
| Status | Approved |
| Owner | CTO |
| Reviewer | CTO |
| Approved By | CTO |
| Last Updated | 2026-08-03 |

---

# Purpose

This document defines the official repository structure, naming conventions, and organizational standards for all repositories maintained under Aqua Rover Technologies.

---

# Repository Structure

```text
AquaOS/
│
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
│
├── docs/
│   ├── 00-foundation/
│   ├── 01-company/
│   ├── 02-engineering/
│   ├── 03-software/
│   ├── 04-ai/
│   ├── 05-cloud/
│   ├── 06-robotics/
│   ├── 07-electronics/
│   ├── 08-devops/
│   ├── 09-testing/
│   ├── 10-security/
│   ├── 11-operations/
│   ├── 12-research/
│   └── 99-archive/
│
├── diagrams/
├── assets/
├── templates/
├── standards/
├── scripts/
└── .github/
```

---

# Folder Rules

- Each folder has a single responsibility.
- Documentation belongs only inside `docs/`.
- Diagrams belong only inside `diagrams/`.
- Reusable templates belong only inside `templates/`.
- Automation scripts belong only inside `scripts/`.

---

# Document Naming

Format:

DOCUMENT-ID-Document-Name.md

Example:

FOUND-001-AquaOS-Constitution.md

---

# Folder Naming

Rules:

- lowercase
- hyphen-separated
- descriptive
- no spaces

Example:

```text
04-ai
07-electronics
99-archive
```

---

# Repository Principles

- Keep repositories organized.
- Avoid duplicate documentation.
- Follow version control best practices.
- Every change must be committed with meaningful commit messages.

---

# Version History

| Version | Date | Changes |
|----------|------|---------|
| 1.0.0 | 2026-08-03 | Initial Repository Standards |