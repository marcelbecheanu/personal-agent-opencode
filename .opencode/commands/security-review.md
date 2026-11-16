---
description: Security review of the pending changes
agent: review
subagent: true
---

Perform a security review of the pending changes (`git diff HEAD`).

Focus on: injection (SQL, shell, path, template), authn/authz gaps, secrets in code or logs, unsafe deserialization, SSRF, XSS, insecure crypto or randomness, missing input validation, and dependency changes.

Report only exploitable or clearly risky findings with `path:line`, attack scenario, severity and fix. Never print secret values. If nothing is found, say so.

Scope: $ARGUMENTS

Changed files:
!`git diff HEAD --stat`
