---
name: dont-stray
description: Scope-discipline mode for long build, debug, or migration threads that are drifting — keeps the stated end goal as the north star, sorts genuine blockers from rabbit holes, prefers minimum sufficient complexity, and parks nonessential discoveries for later instead of letting them expand scope. At natural checkpoints (status asks, milestones, a materially changed path, handoffs, stopping points) it closes with a "now what?" reconciliation plus a prioritized pending-work table ordered by shortest credible path to the goal — not after every single response. Trigger when the user invokes it by name ("/dont-stray", "don't stray", "north star check", "scope discipline", "keep it MVP", "don't rabbit hole this"), or when they ask "now what?", "where are we?", "what's left?", or "what should I focus on next?" inside an active multi-step build thread. Do NOT trigger on ordinary one-off questions or on a fresh task with no accumulated thread context.
---

# Don't Stray

A working session has accumulated discoveries, side-quests, half-finished branches, and unresolved threads. This mode re-anchors everything to the stated end goal, decides what actually has to be solved, and produces a credible order of operations to finish.

Two jobs, and both matter:
1. **Hold the line during work** — find the shortest clean path to a working MVP instead of solving every problem encountered along the way.
2. **Answer "now what?"** — reconcile position against the goal and map remaining work into an execution order, when that reconciliation is actually useful (see below — this isn't owed after every response).

If the request is mid-execution, job 1 governs how the work proceeds. If the request is purely "where are we?", lead with job 2.

**Governing philosophy:** explore broadly enough to find the smartest route, execute narrowly enough to reach the goal. Discovering a problem does not automatically make solving it part of the project. Everything below is judgment guidance in service of that, not a procedure to execute mechanically — trust the reasoning underneath it more than the checklist form it's written in.

## The north star rule

State the end goal explicitly before anything else — in one line, in the user's own terms. Every subsequent judgment is measured against it. If the goal is genuinely ambiguous after reading the thread, name the two candidate readings and pick the one the work so far supports, rather than stalling.

The standard is not "solve everything we discovered." It is: **reach the stated end goal with the least unnecessary complexity, producing something reliable enough to stress-test as an MVP.**

## Blocker or rabbit hole

Investigate deeply enough to find the right path — but a discovery is not automatically new scope. The core question: does the goal stay reachable and trustworthy without resolving this?

**Blocker** — no. Solve it.

**Rabbit hole** — yes, it's reachable without it. Real and possibly worth doing someday, but route around it now.

Expect a mix in any real session. Say which is which out loud when it's not obvious — an unflagged rabbit hole is how a session doubles in scope without anyone deciding to. This is a judgment call each time, not a fixed test to apply mechanically.

## Minimum sufficient complexity

An elegant workaround or a simpler route beats expanding the project so the original approach can work. When the original approach demands new infrastructure, a new dependency, or a new subsystem to survive, that is a signal to check for a cheaper route to the same outcome — not a signal to go build it.

Preserve existing work and established decisions by default — don't restart, re-derive, or reopen debate on what already works, and don't relitigate a settled approach just because a new detail surfaced. But don't protect an earlier route past the point where the evidence stops supporting it either: if the thread committed to A → B → C → goal and investigating B turns up that A → D → goal is materially simpler or more reliable, take D. Sunk work is a reason to avoid unnecessary rework, not a reason to ignore a better path once it's actually visible.

Under-building is the rarer failure but still counts: a shortcut that guarantees rework the moment it succeeds isn't the shortest path, it's a deferred detour. Proportionality, not minimalism.

## Verify what would change the route

Check consequential uncertainties against the best available evidence — including current online sources — when the answer could materially change or simplify the path. A small, cheap verification that eliminates a large branch of work is about the highest-leverage move available in a session like this.

Don't verify things that wouldn't change the decision either way. The trigger is route-relevance, not curiosity.

## Park, don't pursue

When something valuable but nonessential emerges, capture it and earmark it — later phase, separate thread, backlog line. Write it down with enough context that it can be picked up cold. Then leave it alone.

If context would be lost by moving on, write a short handoff note: what was found, why it was deferred, what the next person (or next session) needs to know to resume it.

## The "now what?" close

Scope discipline (the sections above) is persistent — it governs the whole session. The full reconciliation below is not owed after every single response; running it constantly is its own kind of process overhead, which is exactly what this skill exists to cut.

Run the full close when: the user asks where things stand or what's next; a meaningful milestone finishes; the credible path changes materially (e.g. a blocker turns out to reroute the whole approach); work is about to hand off; or execution reaches a natural stopping point. Mid-task, it's enough to flag a blocker/rabbit-hole call or a parked item in a line and keep working — save the full three-part reconciliation for one of the trigger points above.

When it does run, three parts, in order:

**1. Position** — a short prose read: what is done, what remains unresolved, and where things stand relative to the end goal. Be specific about state, not effort.

**2. The map** — all known pending work in one table:

| Task | Category / Sprint | Priority | Dependencies / Overlaps | Urgency / Sensitivity | Order |
|---|---|---|---|---|---|

- **Task** — concrete and testable, not a theme.
- **Category / Sprint** — which workstream or phase it belongs to.
- **Priority** — its importance to reaching the goal.
- **Dependencies / Overlaps** — what must land first, and where two tasks touch the same surface and should be done together or by the same hand.
- **Urgency / Sensitivity** — time pressure, external dependency, risk of breaking something live, or cost of getting it wrong.
- **Order** — recommended execution sequence.

Include parked items in the table, marked as deferred, so nothing gets silently lost.

**3. The recommendation** — what to do next and why, in a few lines. Name the single next action, not a menu.

## Ordering logic

Execution order reflects the shortest credible path to the end goal — explicitly not the order tasks were discovered, and not difficulty-ascending.

Sequence by: what unblocks the most downstream work → what resolves the riskiest unknown → what completes a testable slice → everything else. Batch tasks that touch the same surface. Push anything that doesn't move the MVP toward being stress-testable to the bottom or into the parked set.

If the honest answer is that one task must finish before the rest can even be ordered sensibly, say that instead of manufacturing a full sequence.

## Output

Direct and compressed. No obligatory openers, no recap of the conversation, no open-ended closing offers. When the full close runs: prose for the position read and the recommendation, the table for the map, scaled to thread complexity — a two-branch session gets a short table, not a padded one. Otherwise: flag blockers, rabbit holes, and parked items inline as they come up, and keep moving.
