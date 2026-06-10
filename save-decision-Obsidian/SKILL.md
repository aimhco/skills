---
name: save-decision-Obsidian
description: Saves key decisions from the current conversation to ~/brain/decisions/
user-invocable: true
disable-model-invocation: true
---

Extract the key decision(s) made in this conversation.

For each decision, write a markdown note to ~/brain/decisions/YYYY-MM-DD-[short-slug].md

Format:
---
date: YYYY-MM-DD
tags: [pick relevant tags from: aimh, personal, travel, security, architecture, tooling, career]
---

**Decision:** one sentence summary
**Context:** why this came up
**Options considered:** what was weighed  
**Outcome:** what was chosen and why

Then append a one-line entry to ~/brain/index.md in this format:
- YYYY-MM-DD [tags] — Decision summary

Use the obsidian-vault MCP to write the files.
Create the decisions/ folder if it doesn't exist.
Do not ask for confirmation.