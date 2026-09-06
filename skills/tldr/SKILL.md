---
name: tldr
description: Explain dense technical or architecture material as a concise TL;DR at Grade 6 reading level without losing technical depth. Trigger whenever the user types "/tldr" or asks for a "TL;DR," "quick summary," "explain this simply," "break this down," or wants to understand dense architecture docs, project shorthand, or jargon-heavy material fast — even if they don't use the words "Grade 6" or "TL;DR" explicitly. Also trigger when they paste a wall of technical/architecture text and ask what it means or ask you to make sense of it quickly.
---

# /tldr — Technical TL;DR (Grade 6 Reading Level)

Summarize dense technical or architecture material so the user can understand the logic on the first read — without stripping out the technical substance.

## Core rule

Simplify the **explanation**, not the **underlying technical ideas**.

Keep every important technical term, architecture name, system name, constraint, and piece of context. Do not assume the user already knows internal vocabulary, acronyms, conventions, or compressed project shorthand — even if it's their own project. When a compressed term appears (e.g. "seed the vault," "property MOC," "frontmatter discipline"), explain what it means **in this specific context**, in plain words, right where it appears.

Write sentences short and plain (Grade 6 level: simple words, one idea per sentence, clear cause → effect). Do not write down to the user — this is about speed of comprehension, not simplicity of the ideas.

## Fidelity constraints (do not violate)

- Stay 100% faithful to the source material.
- Do not re-research the topic.
- Do not invent missing architecture or fill gaps with assumptions.
- Do not add recommendations, opinions, or next steps that aren't in the source.
- This is a TL;DR, not a new consulting analysis — don't let it grow into one.

## For each important concept, recommendation, or next step in the source

Where the source contains these, make explicit:

1. **What it means** in practical terms
2. **Why it matters**
3. **How it connects** to the architecture or problem
4. **What outcome would show it worked**

Don't force this 4-part structure onto trivial details — reserve it for the concepts that actually carry the weight of the material.

## Format

- Short, scannable — this is a TL;DR, not a rewrite of the whole document.
- Simple sentences, clear cause-and-effect, no run-ons.
- Explain jargon inline at first use, not in a separate glossary — the user should never hit an unexplained term.
- Default output is inline in chat unless the user asks for a file.

## Verification standard

Before delivering, check: could the user understand every term and every piece of reasoning on the first read, even if they weren't part of the conversation where the project's internal vocabulary developed? If any term or leap in logic would make them stop and ask "wait, what does that mean," expand it.
