# Pitfalls

Lessons from real one-pagers. Check each before rendering and during triage.

## Examples
- **Degenerate example.** An example that lands exactly on a special value (zero, a midpoint, the maximum) looks like nothing happens. Symmetric cases are the usual trap. Pick an example that shows the mechanism working.
- **Accidental ties.** Two examples meant to differ that produce the same or nearly the same value read as "no difference". Compute first, then choose.
- **One dimension only.** When an outcome depends on two inputs, vary each in its own example group; otherwise the page silently suggests only one matters.
- **Example vs proposal.** The central picture and the examples must use the proposed configuration, or carry an explicit label naming the configuration they illustrate.

## Numbers
- Every number and position comes from a script in `scripts/`. Estimated values are wrong often enough to matter.
- When a parameter changes, every dependent value on the page is recomputed and every dependent label updated.
- Parameters that flip an outcome (a weight or threshold that flips an outcome) are flagged in `discussion.md` with their sensitivity.

## Axes and alignment
- Two different axes that look alike (a percentage axis and a result axis) must not line up by coincidence, or readers map one onto the other. Offset one clearly.
- Connectors never run along an unrelated axis line; crossing it at a right angle is fine.

## Spec hygiene
- The page describes the target state. Words like "current", "an earlier version", "today" and old-versus-new comparisons go.
- Differences between design and reality go to `discussion.md`, never onto the page.
- A sign-off checklist is a separate document; the page is signed as a whole.
- The date changes whenever the content changes.
- One term per concept across the whole page; a word used for two things ('level' meaning both a threshold and a tier) gets renamed in one of the places.

## Visual consistency
- Same concept, same shape and colour everywhere; different concepts look different.
- One tint per meaning: markers, legends and fills share exactly the same colours.
- A value printed next to a huge numeral of the same value is redundant.

## Process
- Reviewer briefs go stale when decisions change; update them first.
- Check the render at crop level: arrowheads that stop short, labels touching lines, and orphaned words are invisible in the full view.
- Queued prompts can undo each other; see [revisions.md](revisions.md).
