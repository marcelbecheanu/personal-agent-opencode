---
description: Create or update AGENTS.md with concise project guidance
agent: build
---

Create or update `AGENTS.md` at the repository root so future agents work efficiently here.

Gather only what is needed:
- Build, lint, test and single-test commands (from package.json, Makefile, pyproject, etc.).
- High-level architecture that requires reading several files to understand.
- Non-obvious conventions and gotchas.

Rules:
- Keep it under ~60 lines; every line must save future work.
- Do not list every file, generic advice or things obvious from the code.
- If `AGENTS.md`, `CLAUDE.md`, `.cursorrules` or `.github/copilot-instructions.md` exist, merge their useful content instead of duplicating.

Top-level files:
!`git ls-files | head -50`

$ARGUMENTS
