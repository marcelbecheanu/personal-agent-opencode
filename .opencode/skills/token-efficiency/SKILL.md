---
name: token-efficiency
description: Minimize token consumption, context usage and unnecessary tool calls when working on development tasks.
---

# Token Efficiency

Minimize token usage without sacrificing correctness or safety.

## Instructions

- Be concise. Avoid unnecessary explanations.
- Inspect only files relevant to the task.
- Never read entire directories unnecessarily.
- Prefer targeted searches over reading multiple files.
- Use `git diff` instead of rereading unchanged files.
- Avoid repeating information already available in context.
- Do not repeat completed tool calls.
- Combine independent shell commands when practical.
- Limit command output using filters such as `head`, `tail` and `grep`.
- Avoid unnecessary agents and subagent calls.
- Do not run tests unrelated to the changes.
- Prefer targeted tests over full test suites.
- Do not generate documentation unless requested.
- Summarize tool results instead of reproducing large outputs.
- Ask before expanding the scope of a task.
- Read file ranges, not whole large files, once you know where to look.
- Edit with small targeted replacements; never rewrite a whole file for a small change.
- Do not re-read a file after a successful edit just to check it.
- Keep reasoning short and focused on the next decision; do not re-plan solved steps.
- Use the cheapest agent that can do the job well: economy for commits, pro only for planning and reviews.
- Stop as soon as the task is done and verified.

## Context Management

- Keep only relevant information in context.
- Summarize important findings before long tasks.
- Avoid loading unnecessary dependencies or documentation.
- Do not repeatedly inspect unchanged files.

## Output

- Return the result directly.
- Use short explanations and concise bullet points.
- Report errors only when relevant.
- Never omit important safety information to save tokens.

## Priority

Correctness and safety always take priority over token savings.
