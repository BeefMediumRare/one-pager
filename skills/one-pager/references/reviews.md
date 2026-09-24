# Reviews

A review is four independent reviewers plus your **triage**. The reviewers run as subagents in parallel, each with a fresh context, so they see the page the way a newcomer does.

## The four reviewers

Every reviewer receives: the rendered file (screenshot or Markdown), the page's purpose and audience, the mode, `decisions.md` (so decided points are not re-raised), and its own brief below. No reviewer receives your opinions, earlier findings, or the other reviewers' results.

| Reviewer | Receives additionally | Looks for |
|---|---|---|
| **Content** | `spec.md` as ground truth, `scripts/` to recompute values | correctness of every number and position, completeness, clarity for the audience, misleading or ambiguous wording |
| **Layout** | [one-page-design.md](one-page-design.md) | hierarchy, reading order, grouping, balance, white space, whether the hero carries the page, accidental alignments |
| **Style** | the active style file: [styles/bauhaus.md](styles/bauhaus.md) or the working folder's `style.md` ([poster.md](poster.md)) | every checklist item answered pass/fail; colour-meaning consistency; legibility |
| **Compression** | [compression.md](compression.md) | every text element that fails a checklist item; anything shown twice; anything the drawing already says |

Each reviewer reports a ranked list, each finding with: what, where on the page, why it matters, a concrete fix, and whether it is a real error or a judgement call. Plus a short "verified" list. Cap each report at about 400 words.

Before briefing: make sure every brief reflects the **current** decisions. A brief carrying an outdated palette or rule produces false findings.

## Triage

You present only triaged results. For every finding:

1. **Verify against the render** at crop level: zoom into the region, measure positions against the scripts. Findings that do not hold are dropped.
2. **Check against `decisions.md`**: a finding that contradicts a user decision is dismissed, with the decision named.
3. **Merge** duplicates across reviewers.
4. **Add your own crop-level pass**: arrowheads on target, text collisions, orphaned words, labels touching lines, near-miss alignments between unrelated axes.

Present two lists: **worth fixing** (grouped content / layout / style / compression, most important first) and **dismissed, with the reason**. Then offer the revision prompt.

## Greybox and spec reviews

Greybox and written specs get the content and compression reviewers only; layout and style have nothing to judge yet.
