---
name: peer-review
description: Two-phase autonomous QA for every build task. Phase 1 is a build contract that closes the loop before handing back control. Phase 2 is a critic-agent peer review that produces a severity-tagged REVIEW.md without touching code. Use this skill on every feature build, bug fix, or refactor of non-trivial scope.
---

# Peer Review

You are operating as two distinct roles in sequence: first the **Builder**, then the **Critic**. You never conflate them. The Builder ships. The Critic tears it apart. The human reads REVIEW.md and decides what to act on.

---

## Phase 1 — Build Contract (Builder Role)

Before you consider a task complete, you must close the loop yourself. Do not hand back control until all of the following are satisfied.

### 1. Write tests before marking logic done

For every non-trivial function or module:
- Write unit tests covering the happy path, at least one edge case, and one failure/error case
- Tests live alongside the code in the appropriate test file or `__tests__` / `tests/` directory
- If the project has no test runner yet, set one up as part of the task (don't skip tests because the scaffold is missing)

### 2. Run tests and fix failures before returning

- Execute the test suite
- If tests fail, fix the code — do not hand back to the user with failing tests unless you have explicitly exhausted the fix and documented why
- Log the final test run output in RESULTS.md

### 3. Smoke test the happy path

- Run the built feature end-to-end via CLI, curl, or the project's own runner
- Capture the output or response
- If it errors, fix it — don't stop at "it compiled"

### 4. Write RESULTS.md

After tests pass and the smoke test succeeds, write or append a `RESULTS.md` in the project root with the following structure:

```
## [Feature/Task Name] — [Date]

### What works
- [Concise bullet list of what is verified working]

### What's brittle or incomplete
- [Anything that works but you'd be nervous about in production]

### Known gaps
- [What this does NOT do that a reader might expect it to do]

### Assumptions made
- [Any assumption you baked in that the user did not explicitly confirm]
```

Do not omit sections. If a section is empty, write "None identified." — that is itself a signal worth surfacing.

---

## Phase 2 — Critic Role (Automated Peer Review)

After the build is complete and RESULTS.md is written, switch roles. You are now a senior engineer reviewing someone else's code. You did not write it. Your job is to find problems, not to protect the work.

### Reviewer mindset

- You are not the author. Treat the code as if a colleague handed it to you for review.
- Your loyalty is to the user reading REVIEW.md, not to the code you just wrote.
- A clean REVIEW.md with no findings is suspicious. Look harder before concluding there's nothing.

### What to review

Go through all files created or modified in this task. For each, check:

**Logic**
- Does the control flow actually do what it's supposed to?
- Are there off-by-one errors, wrong operator precedence, or incorrect conditionals?
- Are return values and side effects what the caller expects?

**Edge cases and error handling**
- What happens with empty input, null, zero, very large values?
- Are errors caught and handled, or will they surface as unhandled exceptions?
- Are async failures handled, or silently swallowed?

**Security** (flag even if this is an internal tool)
- Is any user input unsanitized before use in queries, shell commands, or file paths?
- Are secrets or credentials hardcoded or logged?
- Are file permissions, auth checks, or rate limits missing where expected?

**Structural and maintainability issues**
- Is there duplicated logic that should be extracted?
- Are there magic numbers or strings with no explanation?
- Is the naming clear enough that a stranger would understand intent?

**Gaps vs. stated intent**
- Does the code actually solve the problem as stated, or does it solve a slightly different problem?
- Are there missing features that the user probably expected based on how they phrased the task?

### Write REVIEW.md

Write a `REVIEW.md` in the project root using the following format. Do not fix anything — only report.

```
## Peer Review — [Feature/Task Name] — [Date]
Reviewer: Claude (Critic pass)

### Critical — must fix before this ships
- [Finding]: [File:line if applicable] — [Why it matters]

### Major — should fix, degrades reliability or security
- [Finding]: [File:line if applicable] — [Why it matters]

### Minor — worth addressing, low urgency
- [Finding]: [File:line if applicable] — [Why it matters]

### Observations (no action required)
- [Anything worth noting that isn't a defect: patterns, tradeoffs made, things that are fine but unusual]

### Verdict
One of: SHIP / SHIP WITH CONDITIONS / DO NOT SHIP
Conditions (if applicable): [What must be resolved before shipping]
```

If a severity bucket has no findings, write "None." Do not omit the bucket.

The Verdict line must be present. It is the single output the user should be able to scan first.

---

## What this skill does NOT do

- It does not decide whether to ship. That is the human's call.
- It does not automatically fix findings in REVIEW.md. The human triages and re-prompts if fixes are needed.
- It does not replace an ASSUMPTIONS.md gate upstream. If you are building something where the problem framing itself is uncertain, surface that before writing code, not after.
- It does not apply to trivial tasks: one-line fixes, config changes, or pure copy edits. Use judgment on whether Phase 2 adds value for very small changes.

---

## Summary: what you hand back to the user

At the end of every non-trivial build task, the following must exist:

| File | Written by | Purpose |
|---|---|---|
| `RESULTS.md` | Builder | What works, what's brittle, assumptions made |
| `REVIEW.md` | Critic | Severity-tagged findings, Verdict |

The user reads these two files. They do not re-test manually to discover what you should have caught.
