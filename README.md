# Skills

This repository contains a set of decision-making and workflow skills for evaluating ideas, building things, and shipping work with an AI coding assistant. Most are **installable agent skills** (Markdown files with YAML frontmatter) that can be dropped into an assistant's skills directory (e.g. `~/.claude/skills/`) so they auto-surface at the right moment.

The shared principle behind the decision-making skills: the default is not to build. An idea earns more effort by passing a cheap, explicit test with clear continuation criteria.

## Files

### `decision_skills.md`

The complete decision-skill guide for AI-Made-Human experiments and related work. It defines the full workflow for evaluating ideas, MVPs, hackathon concepts, corporate security experiments, product workflows, and career moves.

It covers:

- the prime directive to clarify before coding
- the AIMH experiment loop
- before/after diffs
- specific user selection
- 3-minute pitch creation
- risky assumptions
- cheapest tests
- kill criteria
- tiny MVP scope
- verdicts and artifacts
- tracking, analytics, Linear setup, and prompt templates

This is a standalone reference doc (no frontmatter) - read it directly, or use it to configure an AI assistant's operating instructions for idea evaluation and build decisions.

### `video-moment-detector/SKILL.md`

An installable agent skill that scouts for video-worthy moments in your actual work - decisions, tradeoffs, mistakes, surprises, before/afters, and useful workflows. It inspects session context, git diffs, commit history, and work logs, then recommends one concrete video to record next, complete with hook, format, script outline, and title options. Includes Idea Depot-specific prompts and an optional session wrap-up format. Companion to `decision_skills.md`.

### `idea-intel-funnel/SKILL.md`

An installable agent skill that acts as a junior chief of staff over a solo builder's idea pipeline (Idea Depot). Reads idea data, establishes today's decision context (mode, energy, strategic priority), builds a NOW/NEXT/LATER/PARKING LOT roadmap snapshot, and recommends one focused action for the day - with reasoning, alternatives considered, and a structured disagreement loop so the user can push back and get a re-ranked recommendation.

### `peer-review/SKILL.md`

An installable agent skill providing two-phase autonomous QA for build tasks. Phase 1 (Builder) closes the loop before handing back control: write tests, run them, smoke-test the happy path, and write `RESULTS.md`. Phase 2 (Critic) switches roles to review the diff for logic errors, edge cases, security issues, and gaps versus stated intent, producing a severity-tagged `REVIEW.md` with a SHIP / SHIP WITH CONDITIONS / DO NOT SHIP verdict. Use on every non-trivial feature, bug fix, or refactor.

### `grill-me/SKILL.md`

An installable agent skill for relentless, one-question-at-a-time interrogation of any topic, plan, or position. Leads each question with its own take, resolves each thread before moving on, and tracks open threads until reaching genuine shared understanding. Use when you want a position, plan, or design stress-tested - or whenever you say "grill me".

### `save-decision-Obsidian/SKILL.md`

A user-invocable agent skill that extracts the key decision(s) from the current conversation and saves them as structured notes to an Obsidian vault (`~/brain/decisions/`), with tags and a one-line index entry appended to `~/brain/index.md`. Uses the Obsidian MCP server to write the files without confirmation.

### `design-website/SKILL.md`

An installable agent skill for designing or redesigning any website, web app, or UI into something bold, distinctive, and memorable — across any domain or tech stack. Automatically invokes the `frontend-design` skill for aesthetic philosophy and quality bar, then adds five context questions to resolve before starting (purpose, audience, stack, the one thing visitors must remember, and hard constraints) and a single core rule: commit fully to one direction and name it in three words before touching code. Use when the user wants a strong visual identity, not a generic layout.

### `make-video/SKILL.md`

An installable agent skill and the companion to the [aimh-video-engine](https://github.com/aimhco/aimh-video-engine) project. Turns a rough Tella screen recording (plus its `.srt` subtitles) into a finished, re-voiced video: it rewrites the rambling transcript into a clean, chunked script, synthesizes it in the user's cloned ElevenLabs voice, and re-times the screen footage to the narration. Use from inside the `aimh-video-engine` repo when the user says "make a video" or points at a recording in `videos/<slug>/`.

## Recommended Use

Start with `decision_skills.md` for the full operating manual when evaluating or planning an idea. Drop the skill folders (`video-moment-detector/`, `idea-intel-funnel/`, `peer-review/`, `grill-me/`, `save-decision-Obsidian/`, `design-website/`, `make-video/`) into your assistant's skills directory (e.g. `~/.claude/skills/`) so they activate automatically at the right moments during build, review, and decision sessions.
