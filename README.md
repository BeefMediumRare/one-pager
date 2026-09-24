# one-pager

A Claude Code skill for one-page design documents, after Stone Librande's GDC talk ["One-Page Designs"](https://www.youtube.com/watch?v=E9_wLks1kAg).

Long design docs do not get read. Wiki page trees hide how the parts connect. One page that shows the whole design gets read, discussed, and pinned to the wall.

The poster is the smallest part. Most of the value comes from the loop around it: talking the design through, writing the full spec, checking it against reality, and then removing everything the picture already says.

## What it does

1. **Kickoff**: purpose, audience, status, language, reality sources, voice.
2. **Talk it through** until every part of the spec can be written without guessing.
3. **Full spec**, then a **reality check** against code or docs. Differences go to a discussion list, never onto the page.
4. **Compute** every number the page shows with a script.
5. **Compress**: show, don't tell.
6. **Render** in one of three modes.
7. **Split review** (content, layout, style, compression) by independent subagents, then triage.
8. **Revise** with small, exact prompts.

## Modes

| Mode | When | Output |
|---|---|---|
| Greybox | early idea, for a design meeting | Markdown: one card per section plus an ASCII layout sketch |
| Spec | written one-pager | compressed Markdown spec |
| Poster | settled design | prompts for a Claude Design session, A3 landscape, in the built-in Bauhaus style or one you describe |

In poster mode you keep a Claude Design session open and paste the prompts the skill writes. You stay the designer; the skill orchestrates, computes and reviews.

## Install

As a plugin:

```
/plugin marketplace add BeefMediumRare/one-pager
/plugin install one-pager
```

Or copy `skills/one-pager` into `~/.claude/skills/`.

Optional companion skills:

- [humanizer](https://github.com/blader/humanizer): page text in your voice. Without it, the skill uses a built-in checklist.
- [grill-me](https://github.com/mattpocock/skills/blob/main/docs/productivity/grill-me.md): stress-tests the design while you talk it through. Without it, the skill runs a plain interview.

## Structure

```
skills/one-pager/
  SKILL.md                  workflow, kickoff, modes, state files
  references/
    one-page-design.md      the approach, in our own words
    compression.md          show-don't-tell checklist
    poster.md               poster format, style handling, first-prompt skeleton
    styles/bauhaus.md       default poster style: rulebook and style checklist
    reviews.md              four reviewer briefs and triage
    revisions.md            revision prompt and queue conventions
    pitfalls.md             lessons from real one-pagers
  templates/
    greybox.md  spec.md  decisions.md
```

## Credits

The one-page design approach is Stone Librande's. This repository is an independent adaptation for software design and is not affiliated with him.

## License

MIT
