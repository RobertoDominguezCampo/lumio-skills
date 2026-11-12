---
name: dashboard-design
description: Use this skill for any Power BI dashboard or report design. Design prototype for a dashboard page - layout pattern, components and story, with realistic sample numbers, native Power BI visuals only - before anything is built in Power BI. Use whenever planning, sketching or prototyping a dashboard page, choosing where visuals go, or deciding a page layout. Start from a brief (ask the questions in assets/brief-template.md if there is none), check assets/references/, pick one of the five layout patterns in assets/layouts/, then fill every zone with a component from assets/components/, and always finish with the senior review.
---

# Dashboard Design: the prototype

This skill covers the **design prototype**: which layout, which components, and the story
the page tells. Building it in Power BI comes later. Colours, fonts and spacing tokens come
from your own design system or Power BI theme. This skill decides **where
things go and why**.

## Rule 0: Start from a brief

Context comes first, and it can change the layout.

- **If there is no brief, ask the questions in [assets/brief-template.md](assets/brief-template.md)
  before you design**: audience, decision, first question, never. Do not design on a guess.
- The answer to the first question becomes the page title. The "never" is the cut list.
- **If the brief ends in one action, use the Executive Z insight variant** (one-page
  version in [executive-z.md](assets/layouts/executive-z.md)): no detail table, no side
  navigation, filters in the header, KPI strip, main chart 2/3, action card 1/3.

## Rule 1: Check the references before you design

Open `assets/references/` and read its README. **`fixed-reference.png` is the quality bar**:
every prototype must reach its finish (spacing, type scale, hierarchy, one accent, insight
titles, closed components). Look at `pro/` for how pros build components, and at
`layouts/<pattern>/` once the layout is chosen. Take patterns, not pixels: never copy their
text, data, brands or logos.

## Rule 2: Choose a layout before you place any visual

Do not place a single chart, card or table until you have picked one of these patterns:

| Pattern | Pick it when | File |
|---|---|---|
| **Executive Z** | A few headline numbers, one story, a leadership audience | [executive-z.md](assets/layouts/executive-z.md) |
| **Executive Z (insight variant)** | The brief ends in one action: one question, one page, no table | [executive-z.md](assets/layouts/executive-z.md#one-page-version-no-navigation) |
| **Main + Insight Rail** | A ranking, alert or status has to stay in view during the analysis | [main-insight-rail.md](assets/layouts/main-insight-rail.md) |
| **Hero Split** | One picture carries the answer: a map, a plan, a machine | [hero-split.md](assets/layouts/hero-split.md) |
| **List + Canvas** | Operational tracking of single items: pick one, the page answers | [list-canvas.md](assets/layouts/list-canvas.md) |
| **Full-Bleed** | Control-room or wall screen where the territory is the point | [full-bleed.md](assets/layouts/full-bleed.md) |

If none of the five fits, say so and ask. Do not invent a sixth layout.

## Rule 3: Tell the user which layout you chose and why

Before any visual, write one short block:

> **Layout:** Executive Z
> **Why:** monthly sales review for the leadership team. Four headline numbers, one
> trend that explains them, and a detail table for follow-up questions.
> **Rejected:** Insight Rail. There is no ranking that must stay in view.

Name the pattern, the audience and question that led to it, and the runner-up you rejected.

## Rule 4: Fill every zone with a component

After the layout is chosen, fill each zone with one component from `assets/components/`
(see its README for the index and the shared tokens). **Never a loose visual.** A component
answers one question, helps one action, and comes with its title, main value, context and
chart. Use the size listed for that zone. If no component fits a zone, say so and ask.

## Rule 5: Meet the component quality bar

Every component on every page passes all of these:

- **One family of data.** All components tell the same story with the same dataset. No
  card invents its own business.
- **The title says the insight**, with one key word or number in the accent colour. A title
  driven by a measure is one colour in Power BI, so leave the accent out there.
- **One hero number**, big and bold. Everything else is smaller and grey.
- **Context sits next to the number**: vs last year, vs target, or a status badge.
- **Only one thing highlighted**: one accent bar, one selected card, one selected row. The
  rest is neutral.
- **The story is marked on the chart itself**: a band, a marker, a label. Not a legend.
- **Small controls inside the card when they help**: a period toggle, a metric switch.
- **No empty space.** If the content does not fill the card, use the smaller size.
- **Sizes only from the layout grid**: 376 × 128 KPI, 512 × 440 card, 1024 × 440 main,
  1552 × 352 table.
- **Finish**: 8 px spacing, 12 px corners, thin borders, no heavy shadows, one font,
  tabular numbers.
- **Only native Power BI visuals.** No custom or AppSource visuals, no HTML/SVG measures,
  nothing hard to maintain. If a detail can't be built natively (a progress bar inside a
  card, a checkbox, a band behind a chart), cut it from the prototype. Each component
  file says how to build it.

Before you show a prototype, take a screenshot, compare it with `fixed-reference.png`,
name the 3 biggest gaps in finish, and fix them.

## Rule 6: Components are references, not templates

Adapt each component to the context of the dashboard: its question, its data, its audience.
Change the chart, the control or the story mark when the context asks for it. Do not copy a
component blindly, and never reuse its sample text or numbers.

## Rule 7: Use realistic sample numbers

The prototype shows real-looking figures, not `123` or `Lorem ipsum`: a plausible magnitude,
the right unit, a delta and a comparison (target or prior period). Label the page or the
prototype **"Sample data"**. Sample numbers never move into the Power BI build. There every
figure comes from the model and is reconciled.

## Rule 8: Always finish with the senior review

Before you hand over any prototype, review it against the brief and this skill, list the
problems, fix them, and re-check the screenshot:

1. **Does every component answer a question this person really has?** If not, cut it.
2. **Is there anything on the page that says nothing?** Repeated numbers, labels that
   restate the title, values nobody can act on. Cut them.
3. **Can they see the main message in 5 seconds?** Title, highlighted card and action
   must agree.
4. **Can it be built with native Power BI visuals only?** Name the visual for every zone.
   Every slicer state must still make sense (try each one).

Then write `handoff.md` next to the prototype: open data questions, model, measures and the
native visual for each zone. Do not build it until the user asks.

## Rule 9: Report at the end of every design

Close every design with three lines:

> **Layout:** Main + Insight Rail
> **Components:** 3 × KPI + line chart, Trend comparison, Table with selectors, Insight card, Ranking
> **Brief:** yes, from the user's request / no, assumed audience and question (list the assumptions)

## Shared geometry

- Canvas **1920 × 1080**. Outer margin **24 px**, gutter **16 px**, all values on an 8 px grid.
- Coordinates in each layout file are `x, y, width, height` in pixels from the top-left.
- **Navigation goes on the left by default.** On a 16:9 page, height is the scarce
  dimension and width is the cheap one. A left rail costs width, a top bar costs height that
  the charts need. The left rail also holds any number of pages, while a top bar runs out of
  room after five or six. Use a **text sidebar (320 px)** when page names must be read,
  and an **icon rail (80 px)** when the content needs the width.
- Summary before detail: KPIs at the top, tables at the bottom or in a list column.
- One protagonist per page: the largest box carries the story.

Source of all grids and shares: the *Pro Dashboard Layouts 301* study (301 pro dashboards
out of 1,081 reviewed).
