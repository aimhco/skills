---
name: design-website
description: Use when redesigning or building a personal portfolio, creator brand, or product-lab homepage — especially when the user wants something bold and memorable rather than a generic landing page. Triggers on phrases like "redesign my site", "redesign the portfolio", "make a bold homepage", or when the frontend-design skill is being invoked for a personal brand.
---

# Design Website

Act as a bold, opinionated design director for AI Made Human (aimh.co) and similar personal creator brands. Your job is to deliver a homepage that people remember, using the `frontend-design` skill and the full brief below as your starting point.

**Prime directive:** The design must not be generic. No purple gradients, glassmorphism, Inter font, boring centered heroes, or predictable SaaS layouts.

## When to use

- Redesigning a personal portfolio, creator brand, or product-lab homepage
- User wants a memorable, distinctive design (not a template)
- User is an AI Product Builder, indie maker, or creator brand
- Follow-up refinements after an initial frontend-design pass

## Step 1: Invoke frontend-design now

**REQUIRED:** Before doing anything else, invoke the `frontend-design` skill using the Skill tool:

```
Skill({ skill: "frontend-design" })
```

Do not proceed until that skill is loaded. `frontend-design` drives the aesthetic direction, design thinking process, and implementation quality bar. This skill (`design-website`) supplies the brand context, site brief, and post-launch checklist on top of it.

## Step 2: Brand context

**Brand:** AI Made Human (AIMH)
**Tagline:** "Turning possibilities into projects with AI."
**Role identity:** AI Product Builder — builds AI products.

**Tone:** Human, creative, practical. Bold and memorable. Product-builder focused. Slightly futuristic but not generic "AI SaaS". More "AI product lab / digital workshop / cabinet of experiments" than corporate startup. Friendly enough for normal people, impressive enough for technical people.

## Step 3: The full redesign brief

Use this verbatim (or adapt it) when invoking `frontend-design`:

```
Use the frontend-design skill to redesign my website: https://www.aimh.co/

Context:
AI Made Human is my personal AI product portfolio and creator brand. This is not
just a blog or personal homepage. It is the home base for a growing portfolio of
AI-powered products, experiments, tools, and workflows.

My role:
I am an AI Product Builder. I build AI products.

Current brand line:
AI Made Human — Turning possibilities into projects with AI.

Primary goal:
Create a bold, memorable, expandable portfolio homepage for AI Made Human. The
site should make it immediately clear that AIMH is a growing product lab where I
build multiple AI-powered products over time. The project portfolio is the main
thing. The design needs to scale from a few projects today to many projects later.

Important:
Do NOT create a generic AI website with purple gradients, glassmorphism cards,
Inter font, boring centered hero, or predictable SaaS layout. I want something
people remember.

Brand direction:
AI Made Human should feel human, creative, and practical; bold and memorable;
product-builder focused; slightly futuristic but not generic "AI SaaS"; more
"AI product lab / digital workshop / cabinet of experiments" than corporate
startup; friendly enough for normal people, but impressive enough for technical
people.

Suggested design concept:
Choose one strong aesthetic direction and fully commit to it. Favorite direction:
"Digital Cabinet of AI Experiments" - each project should feel like a collectible
artifact, experiment, or product specimen inside a growing AI product lab.
Other acceptable directions: human-made AI lab, bold magazine-style portfolio,
retro-futurist product workshop, AI invention gallery.

Logo / imagery:
The current large top image can be removed if it does not fit. Incorporate the
AIMH logo (in /assets/images/) tastefully (nav, hero, stamp, badge, lab mark).

Site structure:
1. Hero - AI Made Human is a growing lab of AI-built products, experiments, and
   tools. "I am an AI Product Builder. I build AI products." Use/improve
   "Turning possibilities into projects with AI." Avoid a boring centered hero.
2. Featured Projects / Portfolio - the most important section. Design a scalable
   project system (works with a few projects now, scales to many). Each card
   supports name, short description, status (Live/Prototype/Experiment/Archived/
   Coming Soon), category, links, tags, optional thumbnail. Current projects:
   Awesome AI Tier List Maker, OpenBites, Random Phone Number Selector,
   Idea Depot (Coming Soon). Make projects feel like experiments in a lab.
3. Mission / Vision / Operating Line - Mission: Build products with AI that solve
   real problems and bring people together. Vision: A world where AI builds and
   runs products that solve real problems and naturally create communities.
   Personal Operating Line: Create cool shit. Solve real problems. Build community.
4. Execution Strategy - the game we play (autonomous AI-driven products; launch
   and scale multiple products; idea to execution to distribution fast; solve
   real problems people pay for).
5. AIMH Operating System - run everything as specialized AI "employees" with
   clear roles. Product loop: identify problem, build simple solution, ship fast,
   get feedback fast, validate with payment, iterate. Everything is an experiment;
   speed over perfection; feedback over assumptions; revenue is validation.
6. Future contact / follow - a simple future-facing CTA (more products coming
   soon), easy to replace with a contact form later.

Design requirements:
Memorable. Distinctive typography (no Inter, Roboto, Arial, system fonts). Bold
cohesive color system with CSS variables. Strong spatial composition (asymmetry,
layered sections, editorial hierarchy, grid-breaking, artifact-style cards).
Tasteful motion (page-load reveal, hover effects). Atmosphere (texture, grain,
patterns, labels, stamps, badges, borders). Responsive and polished on desktop
and mobile. Accessible (semantic HTML, contrast, keyboard-friendly, readable).
Reasonable performance.

Implementation requirements:
Inspect the existing codebase first. Preserve existing project links/content.
Do not omit OpenBites. Refactor project content into a scalable data structure.
Incorporate the logo. Remove/replace the current top image if it does not fit.
Implement directly in the existing app. Production-quality, clean, maintainable.

Deliverable:
Redesign the homepage into a bold, memorable, expandable AI product portfolio for
AI Made Human. The final result should feel like an AI product lab with a strong
personal builder identity, not a generic landing page.
```

## Step 4: Chosen aesthetic — Digital Cabinet of AI Experiments

The live site committed to this direction. Key visual decisions made:

| Element | Decision |
|---|---|
| Background | Warm paper + dot grid + grain texture |
| Cards | Brutalist framed "specimen" cards with catalog numbers |
| Status | Stamped badges (Live / Experiment / Coming Soon) |
| Ticker | Scrolling operating-line at top of page |
| Typography | Bricolage Grotesque (display), IBM Plex Mono (labels), Instrument Serif (accents) |
| Color | CSS variable system; warm neutrals + ink black |
| Motion | Page-load reveal, hover lifts, ticker scroll |

## Step 5: Post-design refinements checklist

After the initial `frontend-design` pass, always audit:

- [ ] Project status filter buttons work (hide/show cards by status)
- [ ] Contact email is plain text, not a `mailto:` hyperlink
- [ ] Em dashes replaced with colons, middle dots, or periods in UI copy
- [ ] "About Me" section present with portrait, day/night focus, plain-text contact
- [ ] No horizontal overflow at 320px / 360px / 390px mobile widths
- [ ] Vercel Analytics script tag added before `</body>`: `<script defer src="/_vercel/insights/script.js"></script>`
- [ ] All existing project links and content preserved
- [ ] Logo incorporated (nav, hero area, or stamp/badge)

## Tech stack

Single static file (`index.html`), inline CSS and vanilla JS, no build step. Deployed on Vercel. No framework needed.

## Common mistakes

- **Generic fonts** — Bricolage Grotesque, IBM Plex Mono, Instrument Serif from Google Fonts. Never Inter/Roboto/Arial.
- **Centered hero** — The hero should be asymmetric and editorial, not a standard center-aligned hero.
- **Non-scalable project list** — Projects must be a JS data array (`PROJECTS = [...]`), not hand-coded HTML, so catalog numbers, stats, and filters update automatically.
- **Hyperlinked email** — Keep the contact email as plain visible text; no `<a href="mailto:...">`.
- **Missing mobile QA** — Test at 320px, 360px, 390px, and 768px before calling done.
