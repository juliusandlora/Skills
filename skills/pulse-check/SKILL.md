---
name: pulse-check
description: Run an external "pulse check" before answering — a quick web search against current (2026) documentation and live user/community discussion to compare the textbook/academic approach against how practitioners are actually solving the problem today, then deliver the simplest real-world solution. Trigger ONLY when the user explicitly asks for this by name or clear equivalent phrasing — e.g. "pulse check this," "do a pulse check," "reality check this against how people actually do it," "check this against current docs/discussions before answering," "gap-check your approach." Do NOT trigger automatically on ordinary technical or how-to questions that don't invoke this explicitly — this skill is opt-in per request, not a default research step.
---

# Pulse Check

A pre-answer research step: before giving a technical/practical solution, verify it against what's current and what real practitioners are actually doing, not just pre-trained theory. Surfaces the gap between the "correct" academic answer and the simplest real-world path, then delivers the real-world-informed solution.

## When this applies

Only when the user explicitly invokes it — by name ("pulse check", "pulse-check") or clear equivalent ("reality check this," "check current docs/discussions first," "compare textbook vs. real-world approach before answering"). If the request doesn't contain that signal, don't use this skill — answer normally.

## Workflow

1. **Identify the core question.** Pull out the specific technical/practical problem the user needs solved — the thing that would normally get an answer straight from pre-trained knowledge.

2. **Run the external pulse check.** Use web search (and web_fetch on promising pages) to check:
   - Current official documentation for the relevant tool/library/framework/service (2026 state — versions, defaults, and deprecations change fast).
   - Live user discussion: recent forum threads, GitHub issues/discussions, Stack Overflow, Reddit, blog posts — anywhere practitioners are describing how they actually handle this problem right now.
   - Scale searches to the complexity of the question — a couple of targeted searches for a narrow question, more for something with several moving parts. Prefer sources from the last several months when the topic is fast-moving.

3. **Do the gap analysis.** Compare two things side by side:
   - The complex/academic/textbook approach — what pre-trained knowledge or formal docs would suggest as the "correct" way.
   - The simplest, most elegant real-world path — what people actually reach for in practice, including any shortcuts, newer tools, or conventions that have emerged since training.
   
   Document this comparison **briefly** — a short paragraph or a few bullet points is enough. This is a calibration note for the user, not the deliverable itself. Call out anything genuinely surprising: a deprecated pattern, a newer standard tool, a common real-world workaround that a textbook answer would miss.

4. **Deliver the final solution.** Give the actual recommended approach, informed by step 3 — defaulting to the simpler real-world path unless the academic approach is genuinely better for the user's specific situation (say so explicitly if it is). Don't make the user re-derive the answer from the gap analysis; give them the concrete solution.

## Output shape

- Gap analysis first, kept short (a few sentences or bullets) — not a full essay.
- Then the solution, written normally — code, steps, or explanation as the question calls for.
- Cite sources inline for anything specific pulled from search results, per normal citation practice.
- If the pulse check turns up nothing new — current practice matches the textbook approach — say so in one line instead of manufacturing a gap.
