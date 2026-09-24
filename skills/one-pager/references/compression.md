# Compression

**Show, don't tell.** Every line of text must carry something the picture cannot. Apply this checklist to every line of `spec.md` and, later, to every text on the page. A line survives only if it passes all checks.

## Checklist

1. **Shown?** If the drawing already shows it (an arrow shows the order, a colour marks the group, a line crosses a threshold), cut the sentence. Keep at most a label.
2. **Said twice?** If another element says the same (legend and heading, caption and axis label, a number printed beside a huge numeral), keep the stronger one.
3. **Target state?** It describes the design as intended. Words like "currently", "today", "in an earlier version", "old vs new" go.
4. **Generic?** Explanations describe behaviour, not one example. Example values live in the examples, not in the prose.
5. **Plain?** Jargon becomes the plain behaviour ("rises fast, then levels off", not "logarithmic"), unless the term is the name of a configurable option.
6. **Owned?** Implementation detail the audience does not sign off on (tuning constants, code names) moves to `discussion.md` or a separate document.
7. **Irreplaceable?** Keep what a picture cannot carry: definitions of inputs, units, rules and edge cases, the meaning of a non-obvious feature, the configuration an example was computed with.

Escalation for any explanation: sentence → short label on the drawing → nothing. Stop at the first form that still carries the meaning.

## Written spec variant

The same checklist applies to a text-only one-pager. In addition:
- one idea per line; tables for anything with two dimensions
- a mechanism is shown with one worked example and its numbers, not with paragraphs
- open questions in one list at the end, never scattered

## Humanizer fallback

Use a humanizer skill when installed, with the voice from the kickoff. Without one, check page text for: dashes used as connectors (prefer periods, commas, colons), "not X but Y" constructions, groups of three, inflated words, filler ("in order to", "it is important to note"), and repeated sentence rhythm. Match the requested voice; for a technical audience short and direct beats elegant.
