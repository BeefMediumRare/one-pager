# One-page design

The approach comes from Stone Librande's GDC talk "One-Page Designs" (2010): https://www.youtube.com/watch?v=E9_wLks1kAg. What follows is our own summary, extended with lessons from using it for software design.

## The problem it solves

Long design documents do not get read. A printed design bible is thorough and authoritative, and writing one is genuinely good design work, but nobody reads it cover to cover and nobody can keep it current. Wikis fix updating and history, but they chop a design into pages, need constant gardening, and hide the relationships between the parts: a hyperlink is not a real connection. Readers look at the headline, the pictures and the length of the scroll bar, then leave.

The answer: **one page**, good enough that people want to pin it to the wall.

## What the page is

- **Title = why.** The title states why the page exists. If you cannot write it, stop: you do not yet know what you are trying to say.
- **Date.** Every version carries a date, changed whenever the content changes. It is the only way to know which copy is current.
- **White space.** A wall of text blown up to poster size is not a one-pager.
- **One central illustration** that draws the eye and carries the page. Everything else is a **callout** arranged around it, attached where it explains a specific part.
- **Tiered information.** The title and central picture read at a glance from across the room; details reward a closer look. Decide tier 1, 2 and 3 explicitly.
- **Relationships shown, not described.** Arrows, flows, shared axes, the same shape for the same concept.

## Techniques that fit on one page

- **Flowchart** of the core loop: what the user does, what the system feeds back. A good first one-pager.
- **Storyboard** of the whole experience with timing marks.
- **Space against time**, after Minard's chart of Napoleon's march: one drawing carrying position, quantity and time.
- **Relationship diagram**: how units, modules or parties relate. Redrawing it often reveals a better design (a rock-paper-scissors triangle became sliders along its sides).
- **Top-down matrix**: choose the axes first, then fill every cell. Exhaustive by construction, and a checklist for whoever implements it.
- **Small multiples**: the same thing in several situations, so a behaviour becomes visible in one column.
- **Time** only where it matters (pacing, phases, durations). Not every design has a time axis.

## The test inside the method

**If it will not fit on one page, the design is probably too complex, or you are looking at it wrong.** Struggling to draw something is a signal to simplify the design, not to shrink the font. Librande's own example: a four-dimensional table of 256 cases collapsed into 36 once he found the vector picture behind it.

## How the page is used

- **Working document.** Hand it out, bring pens, invite scribbles. An annotated copy returned to you is the goal: it proves the page was read and feeds the next version.
- **Meeting anchor.** Everybody looks at the same picture instead of imagining different things. Early pages are rough (greybox); the polish comes when the design has settled.
- **Hand it to people.** A link in a chat is easy to ignore; a page in front of someone is not.

## What it does for the designer

- You must understand the problem to draw it.
- Limited space forces you to rank what matters.
- Drawing the connections reveals effects you would otherwise miss.
- It becomes a diff tool: once the intended design is on one page, differences to the implementation or to other documents stand out.

## Composition lessons from practice

- **Labels live on the drawing**, not in a separate legend, wherever the drawing has room.
- **Callouts sit next to what they explain** and share its colour.
- **Supporting diagrams are mini-flows** (condition → result) rather than prose.
- **Same concept, same shape**: if a setting appears in the central picture and in a detail panel, draw it identically in both.
- **Group related callouts**, for example inputs apart from outcomes, so the reader sees which parts belong together.
- **The title can be a compact title block** in a corner, like an architect's plan; the largest element is the picture, not text.
- **The page is a standalone specification of the target state**: no "current implementation", no old-versus-new comparison, no sign-off checklist (that is a separate document).
