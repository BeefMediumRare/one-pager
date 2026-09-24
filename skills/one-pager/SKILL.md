---
name: one-pager
description: One-page design documents in the Stone Librande style. Talk a design through, write the full spec, compress it, then render it as a greybox, a written spec, or a styled poster (via Claude Design prompts) with split reviews. Use when the user wants a one-pager, a design poster, a greybox for a design meeting, or a compact design spec.
---

# One-pager

You are the **orchestrator**. The user is the designer. In poster mode a separate Claude Design session renders the page: you write the prompts, the user pastes them and returns screenshots. The thinking happens here; the page is the smallest part.

Read [references/one-page-design.md](references/one-page-design.md) before step 2. It defines the approach every later step serves.

## State files

Create a working folder `one-pager/<slug>/` (ask where if the project has no obvious place). Keep these files current; they survive context compaction and are what reviewers receive:

- `spec.md` — the full spec (step 3); the complete source and the content reviewer's ground truth. Compression never edits it
- `page.md` — the compressed on-page text (step 6), kept in sync whenever `spec.md` changes
- `decisions.md` — the **decision log**, from [templates/decisions.md](templates/decisions.md); every user decision lands here the moment it is made
- `discussion.md` — the **discussion list**: differences between the design and reality. It never goes on the page
- `scripts/` — every number and position the page shows comes from a script here
- `prompts/NN-<topic>.md` — render and revision prompts, numbered
- `renders/NN.png` — the screenshots the user returns, copied into the folder and numbered to match the prompt they answer
- `style.md` — the active style, only when the user describes their own ([references/poster.md](references/poster.md))
- `greybox.md` / `one-pager.md` — the output of greybox or spec mode (below)

## Steps

1. **Kickoff.** Ask in one round (use AskUserQuestion when available): purpose (becomes the title: why does this page exist?), audience, status (idea / candidate / settled), page language, reality sources (code, docs, tickets, none), humanizer voice or off, mode (greybox / spec / poster; status suggests one, see Modes), grilling yes/no, poster style (default Bauhaus, or the user describes their own in a few words). Done when every answer is recorded in `decisions.md`.
2. **Talk it through.** Interview the user until you could write every section of the spec without guessing. With grilling on and a grilling skill installed, use it. Done when purpose, audience, inputs, mechanism, outputs, and rules and edge cases each have an answer or an explicit open question; parameters and examples too, where the design has them.
3. **Full spec.** Write `spec.md` completely, content only, no layout. Open questions stay marked as open. Done when every item from step 2 has its section in `spec.md`, answered or marked open.
4. **Reality check.** For each reality source, compare every mechanism in the spec against it. Each difference goes to `discussion.md`: where, what the spec says, what the source says, impact. Done when every mechanism has been checked against every source. Skip when the kickoff said none.
5. **Compute.** Write scripts that produce every value, count, position and data point the page will show (e.g. example results, curve points, bar boundaries). Choose examples with [references/pitfalls.md](references/pitfalls.md). Done when every value in `spec.md` traces to a script output.
6. **Compress.** Apply [references/compression.md](references/compression.md) to a copy of `spec.md` and save the result as `page.md`; `spec.md` stays untouched. Done when every line of `page.md` passes the checklist.
7. **Render** `page.md` in the chosen mode (below). Humanize on-page text when enabled: use a humanizer skill if installed, else the fallback in `compression.md`. Check every item in [references/pitfalls.md](references/pitfalls.md) and fix what fails. Then save the prompt or document to its file, copy it to the clipboard when a clipboard tool exists (`pbcopy`, `xclip`, `clip`), and always give the path. Done when every pitfall is checked, the output is saved and the user has its path.
8. **Review** when the user returns a render or asks for one: [references/reviews.md](references/reviews.md). Done when the triaged findings are presented.
9. **Revise** with [references/revisions.md](references/revisions.md). Loop 8–9 until the user calls the page done.

## Modes

Status suggests the mode; the user decides at kickoff.

- **Greybox** (idea stage, for a design meeting): `greybox.md`, one card per section with its content, purpose and layout idea, plus an ASCII sketch of the arrangement this content calls for (no default layout). Rough on purpose, so people write on it. Template: [templates/greybox.md](templates/greybox.md).
- **Spec** (a written one-pager): `one-pager.md`, `page.md` set into the template as compressed prose and tables. Template: [templates/spec.md](templates/spec.md). The working `spec.md` stays the full source behind it.
- **Poster** (settled design): an A3 landscape poster rendered by Claude Design from your prompts, in the active style. Style handling and first-prompt skeleton: [references/poster.md](references/poster.md).

A greybox can graduate to a poster later; `spec.md`, `page.md` and the decision log carry over.
