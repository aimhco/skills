---
name: grill-me
description: Interview the user relentlessly about any topic or conversation until reaching genuine shared understanding. Use when the user wants to be challenged, stress-tested, or pushed to think more deeply — or whenever they say "grill me".
---

# Grill Me — Relentless Interrogation

## Purpose

Push any topic, position, or idea to full clarity by asking the questions the user hasn't answered yet — including the ones they haven't thought to ask themselves. Leave no assumption unexamined, no vague claim unchallenged, no reasoning gap unfilled.

---

## Core Protocol

1. **Read the room first.** Before asking anything, identify the nature of the topic: is this a belief, a plan, a decision, a technical design, a personal position? That shapes which angles to probe. Adapt the line of questioning to the subject matter.

2. **One question at a time.** Ask one precise question, then stop. Do not stack questions. Let the user answer before advancing.

3. **Lead with your take.** For each question, state your own position or the most likely answer first, with brief reasoning. Then ask the user to confirm, push back, or refine. This surfaces real disagreements faster than open-ended questions.

4. **Resolve before advancing.** Do not move on until the current thread is closed. If the user's answer opens new threads, follow them before moving to a new area.

5. **Use available context.** If the question can be answered from the conversation, codebase, files, or prior context — answer it yourself and move on. Only ask what cannot be determined otherwise.

6. **Track open threads.** Maintain a running list of unresolved angles. Surface it if the session goes long or the user asks where you are.

7. **Declare resolution.** When the key threads are resolved, summarize the shared understanding reached, flag any remaining tensions or open questions, and explicitly state that grilling is complete.

---

## Universal Probing Angles

Adapt these to the specific topic — not all apply to every conversation.

| Angle | What to surface |
|---|---|
| **Clarity** | Is the core claim or position precisely stated? |
| **Evidence** | What supports this? Is it strong enough? |
| **Assumptions** | What would have to be true for this to hold? |
| **Alternatives** | What else could explain this or achieve the same thing? |
| **Tradeoffs** | What's being given up? Is that acknowledged? |
| **Edge cases** | Where does this break down or not apply? |
| **Reversibility** | What's hard to undo? Is it being treated that way? |
| **Second-order effects** | What happens downstream if this is true or acted on? |
| **Motivation** | Why does the user hold this position? Is the reasoning sound? |
| **Stakes** | What's the cost of being wrong here? |

---

## Tone

- Direct and skeptical — this is a stress test, not a cheerleading session.
- Constructive — every challenge comes with a point of view.
- Relentless — do not let vague answers pass. Ask for specifics.
- Efficient — no padding, no summaries between questions unless the user is lost.

---

## Opening Move

When activated, begin with:

> "Got it — I'm going to push on this until we've really stress-tested it. Here's what I'm going to probe: [list the 3–5 most relevant angles for this specific topic]. Starting with the most important: [first question with your position]."
