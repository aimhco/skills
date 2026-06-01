# New Idea Runbook

Sit down with a new idea — Saturday morning, lunch break, between meetings. Run it through this *before* building anything. The whole runbook should take 45-60 minutes for a single idea.

If I'm tempted to skip a step "just this once," that's the step that matters most.

---

## Step 1 — Capture (1 min)
One sentence: what's the idea? No fluff, no justification. If I can't say it in one sentence, I don't know what it is yet.

## Step 2 — Write the Diff (5 min)
Two sentences:
- **Before:** what does the target user's life look like right now without this?
- **After:** what does it look like with this, on one screen / in one workflow?

If I can't write a clean before/after, stop. The idea isn't ready. Either it's a topic, not an idea, or the scope is too big.

## Step 3 — Name the User (2 min)
A specific person or tiny segment. "Car shoppers" is wrong. "[Friend name] who's been hunting for a used truck for three weeks" is right. If I can't name a real person who has this problem *right now*, that's the first thing to fix — go find one before going further.

## Step 4 — Write the 3-Minute Pitch (15 min)
Plain text, no slides. The pitch must answer:
- Who this is for
- What's the before
- What's the after
- Why now / why this hasn't been done already
- What would need to be true for this to matter

Record myself saying it out loud. If it runs long, scope is wrong — cut, don't accelerate.

## Step 5 — Identify the Riskiest Assumption (5 min)
List 3-5 things that must be true for this to matter. Rank them by how confident I am in each. The least confident one is what gets tested first. Almost always: "anyone besides me wants this."

## Step 6 — Design the Cheapest Test (10 min)
For the risky assumption I just named, what's the smallest possible action that would shift my confidence? Rules:
- No code unless code is the only way (it usually isn't).
- Should be doable in days, not weeks.
- Should produce a real signal, not vanity output.

Default tests: 5 target-user conversations, a manual mockup, a one-page description shown to potential users, a spreadsheet that simulates the output.

## Step 7 — Write the Kill Criteria (5 min)
One line, before running the test. Format: "I continue if [specific outcome] within [specific window]."

Specifics matter. "People seem interested" is not a criterion. "3 of 5 ask to be texted when it's ready" is.

## Step 8 — Run the Test
Execute. Don't tweak the criteria mid-run. Don't extend the window because "we're close." Don't add features to the test. Just run it.

## Step 9 — Render the Verdict (10 min)
Two options only: **continue** or **archive**. No "park." Write 2-3 sentences explaining the verdict and what the actual signal was.

- If **continue**: write the next risky assumption and the next cheapest test. The framework runs again at the next level.
- If **archive**: write what would make me reverse this decision in the future, if anything. Date it.

## Step 10 — Ship the Artifact
- AIMH idea → record the YouTube episode showing the gauntlet
- Corporate experiment → write up in shared team doc
- Career decision → save the note to my journal
- Hackathon → the pitch and recording are the artifact

The verdict isn't real until the artifact is published or filed.

---

## Idea Template

Copy into a new note in `~/brain/ideas/` for each idea.

```
# [Idea name]

**Captured:** [date]
**Status:** active | archived
**Type:** AIMH | hackathon | corporate | career

## One-sentence idea


## The Diff
**Before:** 
**After:** 

## User
(specific person, not segment)

## Pitch (3 min)


## Risky Assumption
(the one being tested first)

## Cheapest Test


## Kill Criteria
I continue if ___ within ___.

## Verdict
[ ] Continue → next risky assumption: ___
[ ] Archive → reversal conditions: ___
Date: ___

## Artifact
[link or filename]
```

---

## Where Things Live

- **Active ideas:** `~/brain/ideas/active/`
- **Archived ideas:** `~/brain/ideas/archive/` (move the whole note here on archive verdict)
- **Index note:** `~/brain/ideas/index.md` — a table of all ideas with status, captured date, and verdict date. Update on every status change.

The index is the scoreboard. It's also the source material for content — every archive entry is a potential video about an idea that didn't survive the gauntlet, which is rare and honest content.
