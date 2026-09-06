---
name: handoff-02
description: Reconstruct a conversation's current established state as a self-contained Markdown handoff so a new AI thread can continue the work without rereading the original history. Trigger immediately whenever the user types "/handoff-02". Also use whenever the user wants to move work into a fresh thread or session, port or transfer context, catch a new AI up, capture where things stand, or says a conversation has gotten long, bloated, slow, or messy and needs to be restarted somewhere clean. Trigger on "continuity handoff," "state doc," "context transfer," "carry this into a new chat," "pick this up in a fresh thread," and similar intent even when the word "handoff" never appears. Applies to any sustained work -- research, planning, writing, technical builds, creative projects, analysis, decision-making -- not just software projects. Not for chronological recaps, status updates, or "what did we talk about" summaries.
---

# Continuity Handoff

Create a canonical Markdown handoff that allows another capable AI to continue the work from its **current established state** without needing the original conversation.

This skill is for continuity across threads, projects, research, planning, writing, technical work, creative work, decision-making, or other sustained conversations. Adapt the handoff to the work actually present rather than forcing project-specific categories onto it.

## Core Principle

The conversation is **evidence**, not content that must be preserved.

Reconstruct the minimum sufficient current state needed for the next AI to:

- understand what is being pursued and why;
- know what has already been established or completed;
- preserve decisions, constraints, definitions, preferences, and distinctions that still matter;
- continue any active or explicitly pending work without unnecessarily reopening settled ground;
- avoid consequential regressions learned through prior corrections.

Do not summarize the conversation chronologically.

If removing a detail would not materially affect future understanding, judgment, or execution, omit it.

## Authority of Current State

When earlier information conflicts with later revisions, corrections, or confirmed direction, treat the **latest explicit correction or established position as authoritative**.

Do not preserve superseded information as competing context, alternatives, or historical notes unless the history itself remains necessary to understand a current constraint or unresolved issue.

Distinguish between:

- **settled** -- established and no longer requiring reconsideration;
- **active** -- currently being developed, evaluated, or executed;
- **unresolved** -- explicitly left open;
- **superseded** -- replaced by later direction and excluded from the handoff.

Do not infer unresolved status merely because alternatives appeared earlier in the conversation.

## What to Preserve

Select only the dimensions that materially matter to the work. These may include:

- objective and intended outcome;
- relevant background or domain context;
- audience, users, stakeholders, or use case;
- system, artifact, argument, plan, research question, decision, or other work product being developed;
- terminology or definitions established in the conversation;
- key decisions and conclusions;
- constraints and non-negotiables;
- preferences or standards that affect future outputs;
- important assumptions explicitly adopted;
- assets, components, drafts, findings, or work already completed;
- current state of work;
- dependencies that affect continuation;
- explicitly unresolved questions;
- explicitly established next actions.

These are candidate information types, not mandatory sections. Do not include categories simply because they are listed here.

## Learned Judgment

Revision history can contain important information that is invisible in the final state alone.

Preserve a learned distinction when losing it could cause a capable new AI to make a consequential regression.

Give particular attention to situations where:

- older context repeatedly displaced newer direction;
- an important nuance, boundary, or distinction was flattened or ignored;
- the same misunderstanding required multiple corrections;
- an apparently reasonable interpretation repeatedly produced the wrong result.

Do not preserve the correction history itself unless necessary.

Extract the **transferable judgment** behind the correction: enough context for another capable AI to recognize what matters in a similar situation without prescribing exactly how it must reason or act.

Do not convert revision history into an exhaustive behavioral rulebook.

Ignore:

- minor wording corrections;
- isolated mistakes with no continuing relevance;
- abandoned explorations already resolved by the current state;
- branches that worked reliably;
- lessons whose meaning is already obvious from the final established state.

## Boundaries

Do not add:

- new strategies or recommendations;
- speculative explanations;
- unsupported interpretations;
- hypothetical future requirements;
- inferred decisions;
- invented tasks or next steps;
- generic best practices that were not established and are unnecessary for continuity.

Pending work must come from explicit unresolved commitments, open questions, or stated next actions.

Preserve uncertainty where the conversation genuinely leaves something unresolved rather than resolving it yourself.

Do not over-prescribe future execution. Transfer the state, consequential constraints, and learned judgment; leave a capable successor room to exercise its own reasoning.

## Document Structure

Choose the structure that best represents the work.

For substantial ongoing work, a useful default is:

### Current State
The goal, relevant context, established direction, decisions, constraints, definitions, standards, and other truths necessary to understand where the work stands.

### Work State
What exists or has been completed, what is active, important dependencies, unresolved items, and explicitly established next actions.

### Learned Judgment & Regression Risks
Only high-impact, non-obvious distinctions learned through revision that materially affect future judgment or execution.

These sections are defaults, not a mandatory schema. Rename, combine, omit, or add sections when the nature of the work makes another structure clearer.

Do not create empty sections or duplicate the same information across sections.

## Output Standard

Write the handoff as a self-contained Markdown document for an expert successor who has no access to the original conversation.

Use precise sentences and enough context to preserve meaning without reproducing unnecessary history.

Avoid:

- conversation chronology;
- transcript-style summaries;
- filler;
- meta-commentary about creating the handoff;
- references such as "earlier in this thread" or "the user previously said" when the underlying fact can be stated directly;
- excessive procedural instructions for the successor.

The handoff should describe the **resulting state**, not narrate how that state was reached.

## Verification

Before finalizing, ensure that:

- another capable AI could continue the work without reading the original conversation;
- removing the original thread would not remove any context required for the explicitly established next work;
- settled decisions remain settled;
- superseded information does not survive as competing context;
- genuine uncertainty remains marked as unresolved;
- every retained detail materially contributes to understanding, judgment, execution, or prevention of a demonstrated high-impact regression;
- no new idea, task, conclusion, or requirement has been introduced;
- revision-derived lessons preserve useful judgment without constraining the successor into a rigid procedure.

If a detail fails these tests, remove it.

Output only the finished Markdown handoff unless the user explicitly requests another format.
