# ENG-004 — Coding Standards

| Field | Value |
|-------|-------|
| Document ID | ENG-004 |
| Version | 1.0.0 |
| Status | APPROVED |
| Owner | CTO |
| Reviewer | CTO |
| Approved By | CTO |
| Last Updated | 2026-08-11 |

---

# Purpose

This document defines the minimum coding standards followed by the software engineering team at Auqora Technologies.

The goal is to produce code that is readable, maintainable, testable, and easy for another engineer to understand.

---

# General Principles

All engineers should:

- Write simple and readable code.
- Prefer clarity over cleverness.
- Avoid unnecessary complexity.
- Keep functions and modules focused.
- Reuse existing functionality instead of duplicating code.
- Remove unused code and dependencies.
- Handle errors explicitly.
- Never commit secrets, passwords, API keys, or credentials.

---

# Naming Conventions

Names must clearly communicate their purpose.

### Variables and Functions

Use `snake_case` in Python.

```python
plastic_count = 10

def detect_plastic(frame):
    ...
Classes

Use PascalCase.

class MissionManager:
    ...
Constants

Use UPPER_SNAKE_CASE.

MAX_SPEED = 100
DEFAULT_CONFIDENCE = 0.70
Python Standards

Python code should generally follow:

PEP 8
Type hints where practical
Clear docstrings for important modules, classes, and functions
Virtual environments for project dependencies

Example:

def calculate_distance(x1: float, x2: float) -> float:
    """Calculate the distance between two points."""
    return abs(x2 - x1)
Project Structure

Code should be organized into logical modules.

Avoid placing the entire application inside a single large file.

Example:

src/
├── api/
├── ai/
├── navigation/
├── hardware/
├── services/
├── models/
└── utils/

The actual structure may differ between components, but each module must have a clear responsibility.

Error Handling

Errors must be handled intentionally.

Avoid:

try:
    ...
except:
    pass

Prefer specific exception handling and meaningful logging.

Example:

try:
    connect_to_jetson()
except ConnectionError as error:
    logger.error("Jetson connection failed: %s", error)
Logging

Use structured and meaningful logs for important system events.

Examples:

INFO  - Camera initialized
INFO  - Plastic detected
WARNING - Low battery
ERROR - Motor controller unavailable

Do not log passwords, API keys, tokens, or other sensitive information.

Comments

Comments should explain why, not simply repeat what the code does.

Avoid:

# Add one to count
count += 1

Prefer:

# Increment the retry counter before attempting reconnection.
count += 1
Testing

Important functionality must be tested before being merged.

Testing should cover, where applicable:

Normal operation
Invalid input
Failure conditions
Edge cases
Integration with dependent components
Dependencies

Before adding a dependency:

Confirm that it is actually required.
Check whether an existing dependency can solve the problem.
Prefer well-maintained libraries.
Document important dependencies.

Unused dependencies should be removed.

Security

Never commit:

API keys
Passwords
Access tokens
Private certificates
.env files containing secrets

Use environment variables or approved secret-management mechanisms.

Code Review Checklist

Before requesting review, verify:

 Code is readable.
 Naming is clear.
 No unnecessary duplication exists.
 Errors are handled.
 Tests pass.
 No secrets are included.
 Documentation is updated when required.
Rule of Simplicity

When multiple solutions are possible, prefer the simplest solution that:

Meets the requirement.
Is reliable.
Can be tested.
Can be maintained by another engineer.

Do not introduce complexity simply because a technology is available.

Version History
Version	Date	Changes
1.0.0	2026-08-11	Initial Coding Standards