---
description: Simplify changed code (reuse, dead code, duplication) and apply fixes
agent: build
---

Review the uncommitted changes for quality only (not bug hunting) and apply the fixes:

- Reuse existing helpers instead of new duplicated code.
- Remove dead code, needless abstractions and leftover debug output.
- Simplify convoluted logic without changing behavior.
- Fix obvious inefficiencies.

Do not touch code outside the changed regions. Run the narrowest relevant check after editing. Summarize each change in one line.

Scope: $ARGUMENTS

Changed files:
!`git diff HEAD --stat`
