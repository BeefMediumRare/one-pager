# Poster

A poster is one artboard, A3 landscape, rendered by a Claude Design session the user drives: you write the prompts, the user pastes them and returns screenshots.

## Active style

The kickoff decides the style; record it in `decisions.md`.

- **Default:** [styles/bauhaus.md](styles/bauhaus.md).
- **User style:** usually a short description in the chat ("Swiss railway signage", "blueprint, white on navy"); a style guide file or reference image works too. Turn it into `style.md` in the working folder with the same sections as the default style: rulebook (composition, palette with meanings, typography, shapes and lines, guardrails) and a pass/fail style checklist. Fill the gaps in the spirit of the description, list what you filled in, and confirm `style.md` with the user before the first prompt.

Every prompt and the style reviewer use the active style file.

## First prompt: skeleton

The first prompt is complete and self-contained; later prompts are revisions ([revisions.md](revisions.md)). Build it from `page.md` (on-page text) and the script outputs (values) in this order:

1. **Frame**: "Create a one-page design document, one artboard, A3 landscape, in the style described below. All page text is in <language>; use the text below verbatim."
2. **Philosophy**: the principles from [one-page-design.md](one-page-design.md) that govern layout: hero carries the page, callouts attached, white space, tiers, labels on the drawing.
3. **Style**: paste the active style's rulebook, including the palette table with the concept mapping filled in.
4. **Content**, section by section, with exact values:
   - every text verbatim
   - every value, count, position and data point explicitly (e.g. curve points as value pairs, positions as a percentage of the axis width, bar boundaries). Claude Design approximates anything left vague
   - which element each callout attaches to
5. **Layout**: where the hero sits, how the callouts arrange around it, where the title block goes. Derive it from this design's content (the hero technique and the relationships between sections), not from an earlier poster; if a greybox exists, start from its layout sketch. The active style sets the composition rules, not the arrangement.

Keep a copy of the full prompt as `prompts/01-poster.md`.
