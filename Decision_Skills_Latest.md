# Decision Skills for AI-Made-Human Experiments

Use this skill whenever the user wants to evaluate, prioritize, build, pitch, track, or continue an idea, MVP, hackathon concept, corporate security experiment, product workflow, or career move.

The core philosophy: **the default is not to build.** An idea earns the right to move forward by surviving a small, clear test.

This skill is optimized for using Codex, Claude Code CLI, or any agentic coding assistant without overbuilding.

---

## Prime Directive

Do **not** start by coding.

Start by forcing clarity:

1. What exact moment or workflow is broken?
2. Who specifically has this problem?
3. What changes for them after the idea exists?
4. What must be true for the idea to matter?
5. What is the cheapest test of that assumption?
6. What outcome earns continuation?

If the idea cannot pass this clarity layer, do not build it yet.

---

## Mental Model

Every idea is a small experiment, not a commitment.

This applies to:

- AIMH MVPs
- YouTube build-in-public videos
- hackathon pitches
- corporate security workflow experiments
- offensive security AI experiments
- career decisions
- internal tools
- dashboards and tracking systems

The goal is not to prove the idea is good. The goal is to discover the truth cheaply.

---

## The AIMH Experiment Loop

For every idea, follow this order:

1. **Idea sentence**
2. **Before / after diff**
3. **Specific user**
4. **Mini pitch**
5. **Riskiest assumption**
6. **Cheapest test**
7. **Kill criteria**
8. **Tiny MVP only if needed**
9. **Artifact**
10. **Verdict: continue or archive**

Do not skip straight from idea to prototype.

---

## Step 1 — Capture the Idea

Write one sentence only.

Bad:

> Build an app for belonging.

Better:

> Help remote workers find one nearby person to silently cowork with today.

If the idea cannot be explained in one sentence, it is still a topic, not an idea.

---

## Step 2 — Write the Diff

Write the before and after state.

Template:

```md
Before: [specific user] currently does [painful/clunky/isolating behavior].
After: [specific user] can do [specific improved behavior] in [one screen / one workflow / one moment].
```

Example:

```md
Before: A remote worker spends the whole day alone at home and never knows who nearby is also working quietly.
After: They open one page and see one nearby quiet coworking session they can join today.
```

If the before/after is vague, stop and narrow the idea.

---

## Step 3 — Name the User

Use a real person or tiny segment.

Bad:

- travelers
- remote workers
- lonely people
- security teams

Better:

- a solo business traveler in Chicago tonight
- a WFH cybersecurity manager in Tampa who misses hackathon energy
- a pentester who spends 3 hours cleaning up report language
- a parent who wants one low-pressure local walk with another parent

The smaller the user, the clearer the MVP.

---

## Step 4 — Write the Mini Pitch Before Building

Write a plain-text 3-minute pitch before touching code.

The pitch must answer:

1. Who is this for?
2. What is the painful before state?
3. What is the improved after state?
4. Why now?
5. Why is the current workaround bad?
6. What is the smallest useful version?
7. What would need to be true for this to matter?

If the pitch does not fit in 3 minutes, the scope is too large. Cut scope; do not talk faster.

---

## Step 5 — Identify the Riskiest Assumption

List 3-5 assumptions that must be true.

Typical assumptions:

- Someone besides me wants this.
- The user has this problem often enough.
- The user will take the required action.
- The solution is simpler than existing behavior.
- The user would come back.
- The user would share it.
- The user would pay for it.

Pick the assumption with the lowest confidence and highest importance.

Usually the riskiest assumption is not “can this be built?”

Usually it is:

> Does anyone care enough to act?

---

## Step 6 — Design the Cheapest Test

The cheapest test is the smallest action that changes confidence in the riskiest assumption.

Prefer:

- 5 target-user conversations
- a text description
- a landing page
- a Figma/mockup
- a spreadsheet simulation
- a manual concierge version
- a fake-door button
- a short video explaining the idea

Avoid code unless code is truly required.

Rules:

- doable in days, not weeks
- tests behavior, not compliments
- produces a clear signal
- does not require a full app

---

## Step 7 — Write Kill Criteria Before Testing

Write one clear continuation rule.

Template:

```md
I continue if [specific outcome] within [specific time window].
```

Examples:

```md
I continue if 3 of 5 target users ask to be notified when this is ready within 2 weeks.
```

```md
I continue if 2 people voluntarily use the prototype twice within 7 days.
```

```md
I continue if one teammate reports that the workflow made reporting clearly faster or better by Friday.
```

Bad criteria:

- people seem interested
- the idea feels promising
- it got some likes
- I still think it has potential

No criteria means the idea will drift forever.

---

## Step 8 — Build Only the Tiny MVP

Only build after cheap tests earn it.

The MVP should improve one moment, not create a universe.

For belonging apps, do not start with:

- feeds
- profiles
- infinite chat
- full community systems
- complex matching
- gamification
- dashboards

Start with one action:

- join a nearby coworking session
- ask who wants dinner nearby
- create a walking slot
- share a silent work room
- see one local ritual happening today

The test is whether the user experiences relief, clarity, or connection quickly.

---

## MVP Quality Bar

A good MVP should be explainable in 15 seconds.

Checklist:

- one user
- one pain
- one action
- one screen if possible
- one success metric
- no unnecessary settings
- no clever architecture unless needed
- no future platform thinking

If the MVP sounds impressive but cannot be used quickly, it is probably too large.

---

## AIMH Video Format

For YouTube, do not only present the final pitch deck.

Use this structure:

1. **Idea** — what human problem triggered the experiment?
2. **Questions** — what pitch questions exposed the real scope?
3. **Tiny test/MVP** — what was built or tested?
4. **3-minute pitch** — what is the clearest version now?
5. **Reflection** — what was wrong, surprising, or worth continuing?
6. **Verdict** — continue or archive

The thinking process is part of the product.

Suggested title patterns:

- This Idea Sounded Great Until I Built It
- I Tried Solving Loneliness With One Tiny Feature
- Why Most App Ideas Fall Apart
- I Forced Myself to Pitch This in 3 Minutes
- Can Tiny Apps Create Real Belonging?

---

## Verdicts

Use only two final statuses:

- **Continue**
- **Archive**

Avoid “parked” as a default status. Parked usually means archived without the emotional clarity.

If an idea is not actively being tested with kill criteria, archive it.

When archiving, write reversal conditions:

```md
Archived because: [actual signal]
I would reconsider if: [specific future condition]
Date: [date]
```

Archiving is not failure. It is cheap learning.

---

## Tracking System

Use the simplest system that creates momentum.

Recommended starting stack:

- **Linear** for execution, prioritization, cycles, and project status
- **GitHub** for code
- **Vercel** for deployment
- **Vercel Analytics** or simple event logging for early usage
- **Supabase** for lightweight custom events if needed
- **Google Drive** for videos, pitch decks, and assets
- **Optional Notion** only for long-form thinking or reference notes

Do not build a custom dashboard yet unless the dashboard itself passes this same framework.

---

## Linear Setup

Use Linear as the AIMH Product Studio OS.

### Projects

Each MVP or experiment is a Linear project.

Examples:

- SameTable
- Local Coworking Session
- Traveler Dinner Ping
- Offensive Security Report Helper
- AI Recon Workflow Test

### Issues

Issues are tiny actions.

Examples:

- Write one-sentence idea
- Write before/after diff
- Draft 3-minute pitch
- Identify risky assumption
- Design cheapest test
- Add Vercel Analytics
- Build fake-door page
- Record AIMH episode
- Write verdict

### Labels

Suggested labels:

- `aimh`
- `corporate-experiment`
- `security`
- `belonging`
- `hackathon`
- `career`
- `active`
- `continue`
- `archive`
- `high-energy`
- `video-needed`
- `analytics-needed`
- `cheap-test-first`

### Cycles

Run weekly experiment cycles.

Example weekly cadence:

- Monday: choose one experiment
- Tuesday-Wednesday: run cheapest test / tiny build
- Thursday: collect signal
- Friday: write verdict
- Weekend: record or edit artifact

Do not run too many active experiments at once.

Recommended limit: 1-3 active experiments.

---

## Analytics

Early analytics should be boring.

Do not start with PostHog unless the product has enough usage to justify it.

Start with:

- Vercel Analytics for page views and visitors
- simple Supabase event table for critical actions

Track only a few events:

- `viewed_page`
- `clicked_join`
- `created_session`
- `shared_link`
- `returned`
- `requested_access`

Early product truth is mostly qualitative.

The most important question:

> Did anybody come back voluntarily?

Good early signals:

- someone asks for access
- someone returns without being reminded
- someone shares it
- someone asks when it will be ready
- someone uses the manual version
- someone gives a specific use case

Weak signals:

- likes
- vague praise
- “cool idea”
- technical compliments
- views without action

---

## Corporate Security Experiments

Use the same mindset at work, but keep it operationally sane.

Do not create daily experimentation chaos.

Use weekly micro-experiments.

Good experiment targets:

- recon workflow
- reporting workflow
- triage process
- scoping process
- detection hypothesis
- AI-assisted note cleanup
- AttackForge/Vectr workflow
- purple team handoff
- exploit reproduction notes
- finding deduplication

Template:

```md
Experiment: [name]
Workflow: [specific repeated workflow]
Before: [current friction]
After: [specific improvement]
User: [team/person]
Risky assumption: [what might not be true]
Cheapest test: [one person / one week / one workflow]
Kill criteria: continue if [specific signal] by [date]
Verdict: continue | archive
Artifact: [team writeup link]
```

Rule of thumb:

- 90-95% core mission
- 5-10% experimentation

Avoid innovation theater.

---

## Career Decisions

Treat career options as experiments too.

Do not evaluate only by title or company prestige.

Evaluate by the lived week.

Template:

```md
Role/company:
Before week:
After week:
What work would I actually do?
Does this move me toward building, creating, and experimenting?
Or does it only upgrade the surroundings of orchestration?
Riskiest assumption:
Cheapest test:
Kill criteria:
Verdict:
```

Good fit signals:

- autonomy
- ambiguity
- product thinking
- experimentation
- security + AI + human systems
- cross-functional influence
- builder culture

Bad fit signals:

- bureaucracy
- maintenance-only work
- meeting-heavy orchestration without creation
- unclear ownership
- innovation branding without actual building

---

## Anti-Patterns

Watch for these:

1. **Building before validating**
   - If the first test requires code, challenge it.

2. **Making the tracker the project**
   - Improving the system can become procrastination.

3. **Over-instrumenting too early**
   - Analytics earn their place after signs of life.

4. **Overbuilding belonging apps**
   - Belonging comes from repeated small interactions, not complex social features.

5. **Confusing compliments with demand**
   - Look for behavior, not praise.

6. **Continuing because of sunk cost**
   - Effort spent is not evidence.

7. **Pitching after building**
   - Write the mini pitch first. It is the cheapest clarity test.

8. **Too many active ideas**
   - Active means actively testing. Everything else is archived.

9. **Daily corporate experiments**
   - Daily experiments become theater. Weekly is healthier.

10. **Using AI to create complexity**
    - AI should reduce friction, not create a bigger system.

---

## Default Prompt for Codex / Claude Code CLI

Use this when starting an idea:

```md
You are helping me evaluate and possibly build a tiny MVP using my Decision Skills framework.

Do not start coding yet.

First, help me produce:

1. one-sentence idea
2. before/after diff
3. specific user
4. 3-minute plain-text pitch
5. 3-5 assumptions
6. riskiest assumption
7. cheapest test
8. kill criteria
9. smallest possible MVP only if the cheap test earns it
10. artifact plan

Bias toward reducing scope.
Challenge vague ideas.
Prefer manual tests before code.
Do not create complex architecture unless required.
```

---

## Default Prompt for Building After Validation

Use this only after the idea has earned a tiny build:

```md
Build the smallest possible MVP for this validated experiment.

Constraints:

- one user flow only
- one primary action
- no authentication unless absolutely required
- no complex dashboard
- no feed
- no unnecessary settings
- deployable quickly
- add only basic analytics for the primary action
- optimize for clarity, not completeness

Before coding, restate the exact MVP scope and what you will intentionally not build.
```

---

## Default Prompt for Verdict

Use this after a test:

```md
Help me render a clear verdict for this experiment.

Use only:

- Continue
- Archive

Evaluate against the original kill criteria.
Do not let me move the goalposts.
Write 2-3 sentences explaining the signal.
If archived, write reversal conditions.
If continued, identify the next riskiest assumption and cheapest test.
```

---

## Idea Template

```md
# [Idea Name]

Captured: [date]
Type: AIMH | Corporate | Hackathon | Career | Internal Tool
Status: Active | Continue | Archived

## One-Sentence Idea


## Before / After Diff

Before:
After:

## Specific User


## 3-Minute Pitch

Who this is for:
Before:
After:
Why now:
Current bad workaround:
Smallest useful version:
What must be true:

## Assumptions

1.
2.
3.
4.
5.

## Riskiest Assumption


## Cheapest Test


## Kill Criteria

I continue if ___ within ___.

## MVP Scope, If Earned

Build:
Do not build:

## Analytics / Signals

Primary action:
Return signal:
Qualitative signal:

## Verdict

Continue | Archive

Reason:
Signal observed:
Next risky assumption, if continuing:
Reversal condition, if archived:
Date:

## Artifact

YouTube video / internal writeup / pitch / journal note:
Link:
```

---

## Final Reminder

The skill is not building.

The skill is turning vague energy into a small test, getting real signal, and making a clean decision.

Small experiments compound.
