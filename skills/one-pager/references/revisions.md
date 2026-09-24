# Revisions

In poster mode the user pastes revision prompts into the Claude Design session that holds the page. A revision prompt is small, exact and self-contained.

## Writing a revision prompt

- **Scope line first**: which sections change, then "Change nothing else."
- **Exact values**: texts verbatim, every value, count, position and data point explicit (e.g. positions as a percentage of the axis width, curve points as value pairs, bar boundaries), colours by name from the palette. Anything vague gets approximated.
- **Target state only**: describe the result, never the history ("the connector runs from A to B", not "fix the connector that was wrong").
- **Numbered steps** when there are several changes; keep numbering consistent after edits.
- **One file per prompt**: `prompts/NN-<topic>.md`. Copy it to the clipboard when possible and give the path.

## Queue discipline

The user may hold several unsent prompts.

- A prompt that supersedes an unsent one says so at the top ("replaces 27 and 28") and contains everything still needed from them.
- Before handing out a prompt, check it against every unsent one for conflicts (one removes a label another re-adds). Resolve by merging into one prompt.
- When a user asks for an old prompt again, re-read it and warn if a later decision contradicts it.

## After a render comes back

- The screenshot is the truth. Changes the user made by hand in Claude Design are decisions: record them in `decisions.md` and never undo them in a later prompt.
- When the user reverts one of your changes, record why, and do not re-propose it.
- Recompute any value that a content change touches (new example, new parameter) before writing the prompt.
