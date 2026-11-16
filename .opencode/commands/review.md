---
description: Review current changes (or a target) for bugs and regressions
agent: review
subagent: true
---

Review these changes for correctness bugs, security issues and regressions.

Target: $ARGUMENTS (empty = uncommitted changes)

Changed files:
!`git status --short`

Diff stat:
!`git diff HEAD --stat`

Read the full diff yourself with `git diff HEAD` (or the target above). Report only verified findings, most severe first, as `path:line — problem — failure scenario — fix`. If nothing is wrong, say so.
