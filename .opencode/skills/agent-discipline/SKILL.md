---
name: agent-discipline
description: Reliable tool use, editing and verification habits for DeepSeek coding agents. Load before any multi-step coding task.
---

# Agent Discipline

Habits that prevent the most common agent failures: invented file contents, broken edits, loops and unverified claims.

## Ground Truth

- Never guess file contents, paths, APIs or command output. Read or search first.
- Read a file (or the relevant range) before editing it.
- Copy edit anchors exactly from the latest read, including indentation and whitespace.
- After a failed edit, re-read the target region before retrying. Never retry the same edit unchanged.
- Check that a dependency, function or config key exists before using it.

## Tool Calls

- One clear purpose per tool call. Batch independent reads or searches together.
- Use the dedicated read/search/edit tools instead of shell equivalents when available.
- Prefer non-interactive commands and flags (no editors, pagers or prompts).
- Run long or blocking commands with a timeout or in the background.

## Loop Protection

- If the same error appears twice, stop and change approach: re-read, narrow the problem or ask.
- If three attempts fail, report what was tried, the exact error and the next best option.
- Do not keep editing to make a test pass without understanding why it fails.

## Verification

- After changes, run the narrowest relevant check: type check, linter, targeted test or build.
- Only report success for things actually verified. State clearly what was not verified.
- Report failing output honestly; never hide or suppress errors.

## Communication

- Reply in the user's language. Keep code, identifiers and commit messages in English.
- Never mix languages or output stray Chinese text in code, comments or replies.
- Ask one concise question when a requirement is ambiguous and a wrong guess is costly; otherwise choose a sensible default and say so.

## Safety

- Never print, log or commit secrets.
- Ask before destructive or irreversible actions (deleting files, history rewrites, migrations, force operations).
