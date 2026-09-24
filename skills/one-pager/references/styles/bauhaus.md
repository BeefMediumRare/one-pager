# Style: Bauhaus

The default poster style: a Bauhaus / Swiss poster. Bold, flat, geometric, calm. Every shape carries meaning. A custom style file follows the same sections: rulebook (composition, palette with meanings, typography, shapes and lines, guardrails) and a pass/fail style checklist.

## Rulebook

### Composition
These are rules for how the page is composed, not a layout. The arrangement comes from the design's content ([poster.md](../poster.md), step 5).
- A3 landscape, one artboard, generous margins.
- **Asymmetric balance**: the hero is clearly the largest element and is not centred on the page. Avoid symmetric splits and even grids of equal boxes.
- Gutters between groups are clearly wider than the gaps inside a group.
- The title block is compact (kicker, headline, date, status) and never the largest element.
- Very large numerals may be set as graphic elements: section numbers or one key figure. Use them sparingly.
- Groups are separated by thick black rules and white space. Columns and rules end where their content ends.

### Palette: five colours, fixed roles
| Colour | Hex | Role |
|---|---|---|
| Cream | `#F2EBDD` | background |
| Black | `#111111` | text, rules, connectors, and the base: the context or reference the focus is shown against |
| Blue | `#1F4E9C` | the focus: the element the page is about, or what is added |
| Red | `#D7261E` | warning: negative, risk, a limit exceeded |
| Yellow | `#F2C230` | highlight: positive, a goal met, what the eye should find first |

Map the design's concepts onto these roles once, record the mapping in `decisions.md`, and use it identically everywhere: areas, bars, markers, legends, mini-charts. If the design has no positive/negative pair, red and yellow become two contrasting categories; record which is which. A role the design does not need stays unused rather than being reassigned to decoration.

### Typography
- **Jost** (Google Fonts) only. Headlines 800–900 with tight tracking, body 400–500, section labels in uppercase with wide tracking.
- The headline may be set in Bauhaus lowercase; everything else keeps normal casing.
- Numbers in the same family; huge numerals are graphic elements.

### Shapes and lines
- Primary shapes carry meaning: circle, triangle, square.
- Fills are flat solid colour. A region that is not the focus is drawn as a thin black outline.
- **Connectors are orthogonal**: vertical and horizontal segments with sharp corners, at the weight of the section rules. Curves appear only where the data itself is curved.
- Arrowheads and markers are small solid black triangles.
- Rings and arcs are drawn thick, about 40 % of the radius; indicators are solid black.
- Labels sit on the drawing: inside a coloured area, at the end of an axis, next to the mark they name.

### Guardrails
These slipped through reviews before; the style reviewer checks each one explicitly. Each has its positive target above.
- No curved or rounded connectors (target: orthogonal routing).
- No gradients, hatching, transparency or tints (target: flat fills and outlines).
- No shadows, no card frames, no rounded corners (target: rules and white space).
- No decorative tick marks or ornaments (target: every mark carries meaning).
- No sixth colour, no grey tints (target: the five-colour table).

## Style checklist (for the style reviewer)

Answer each with pass or fail, citing where on the page:
1. Only the five colours appear, each in its recorded role.
2. Every connector is orthogonal with sharp corners.
3. Every fill is flat; unfocused regions are outlines.
4. No shadows, frames, rounded corners, gradients, hatching.
5. Jost only; the hierarchy headline → section label → body is consistent.
6. The hero dominates and the composition is asymmetric, without an even grid of boxes.
7. The same concept has the same shape everywhere on the page.
8. Arrowheads land exactly on their targets; nothing collides or overlaps.
9. Labels sit on the drawing where there is room.
10. No text line ends with a single orphaned word.
