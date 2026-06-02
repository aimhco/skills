# Skills

This repository contains a small set of decision-making skills for evaluating ideas before building them. They are written as Markdown reference files that can be used directly by a person or loaded into an AI coding assistant as operating instructions.

The shared principle across all three files is simple: the default is not to build. An idea should earn more effort by passing a cheap, explicit test with clear continuation criteria.

## Files

### `Decision_Skills_Latest.md`

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

Use this file when you want the full framework and detailed guidance.

### `decision_skills_reference.md`

A compact reference version of the decision framework. It summarizes the six core parts of the system:

- the diff
- the risky assumption
- the cheapest test
- the kill criteria
- the verdict
- the artifact

It also shows how the framework applies to AIMH MVPs, hackathon pitches, corporate experiments, and career decisions.

Use this file when you need a quick reminder of the framework without the full detailed playbook.

### `decision_skills_runbook.md`

A step-by-step runbook for processing one new idea in about 45-60 minutes. It turns the framework into a practical checklist, from capturing the idea through shipping an artifact.

It includes:

- timed steps for evaluating a new idea
- rules for stopping when the idea is still unclear
- guidance for writing the 3-minute pitch
- cheapest-test and kill-criteria prompts
- a reusable idea-note template
- suggested locations for active and archived idea notes

Use this file when you are sitting down with a specific idea and need to decide whether to continue, archive, or run the next test.

### `aimh-video/SKILL.md`

A companion **installable agent skill** (with frontmatter, unlike the reference
files above). It helps you spot a film-worthy moment while building or deciding,
and shapes it into a 3-5 minute YouTube video about your thinking — covering when
to film, the five-beat narrative arc, hook formulas, b-roll suggestions, and a
five-slide pitch-deck outline.

Drop the `aimh-video/` folder into an assistant's skills directory (e.g.
`~/.claude/skills/`) so it auto-surfaces during build/decision sessions, or read
it directly when planning a video. It pairs with `Decision_Skills_Latest.md`.

## Recommended Use

Start with `decision_skills_runbook.md` for a specific idea. Keep `decision_skills_reference.md` nearby as the quick framework summary. Use `Decision_Skills_Latest.md` when you need the full operating manual or want to configure an AI assistant to follow the process.
