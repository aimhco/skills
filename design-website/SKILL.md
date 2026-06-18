---
name: design-website
description: Use when designing or redesigning any website, web app, or UI — especially when the goal is something bold, distinctive, and memorable rather than a generic layout. Triggers on phrases like "redesign my site", "design a homepage", "make something bold", or any frontend build where the user wants strong visual identity.
---

# Design Website

Your job is to design something people remember. Not a template. Not generic AI output.

**REQUIRED:** Invoke `frontend-design` now before doing anything else:

```
Skill({ skill: "frontend-design" })
```

That skill defines the aesthetic philosophy, design thinking process, and quality bar. Follow it completely.

## What this skill adds

`frontend-design` teaches you *how* to design. This skill adds the questions you must answer *before* opening the brief:

### Before you start, ask the user (if not already provided):

| Question | Why it matters |
|---|---|
| What is the site for? (product, portfolio, tool, brand, etc.) | Shapes the tone extreme to choose |
| Who is the audience? | Determines density, sophistication, approachability |
| What tech stack? (static HTML, React, Next.js, etc.) | Determines implementation approach |
| What's one thing visitors must feel or remember? | The north star for every design decision |
| Any hard constraints? (existing brand, colors, frameworks) | Avoids rework |

If the user has already provided enough context, skip straight to designing.

### The one rule

Commit fully to one bold direction. Don't hedge. Don't default.

Every element — typography, color, layout, motion, texture — should reinforce that single direction. If you can't name the direction in 3 words, you haven't chosen one yet.

## Common mistakes

- **Asking too many questions** — if context is clear, design first
- **Picking a safe middle** — bold and refined both work; mushy does not
- **Generic fonts** — no Inter, Roboto, Arial, or system fonts
- **Centered hero by default** — earn it or break it
- **Ignoring stack constraints** — a static HTML site and a Next.js app need different implementations
