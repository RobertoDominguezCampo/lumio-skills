# Layout — Full-Bleed

The visual is the background and panels float on top of it. 10 of 301 pro dashboards (3%).

## When to use it

- **Type of dashboard:** control-room screens and spatial stories where the territory is
  the point. Energy sites, city or delivery networks, buildings, a fleet on a map. Also
  strong as a report cover page.
- **Audience:** operations centres and wall screens read from a distance, or a leadership
  audience opening the report. They need the picture first and only 3–4 numbers.
- **Reading path:** the visual first, then the floating panel, then the KPI cards along
  the bottom.

## Grid (1920 × 1080)

```
┌──────────────────────────────────────────────────────────┐
│┌┐┌──────────────┐ (filter)(filter)(filter)               │
│││ │              │                                        │
│││ │  Floating    │          ┌─────────┐                   │
│I│ │  panel       │          │ Callout │                   │
│c│ │              │          └─────────┘                   │
│o│ │              │ ┌──────────┐┌──────────┐┌──────────┐   │
│n│ │              │ │ KPI card ││ KPI card ││ KPI card │   │
│└┘└──────────────┘ └──────────┘└──────────┘└──────────┘   │
└───────────── full-bleed visual behind everything ────────┘
```

| Zone | x | y | w | h |
|---|---|---|---|---|
| Full-bleed visual (background) | 0 | 0 | 1920 | 1080 |
| Floating icon rail nav | 24 | 24 | 64 | 1032 |
| Floating panel | 104 | 24 | 544 | 1032 |
| Filter pill 1 | 664 | 24 | 148 | 44 |
| Filter pill 2 | 824 | 24 | 148 | 44 |
| Filter pill 3 | 984 | 24 | 148 | 44 |
| Callout (anchored to a point on the visual) | 1220 | 430 | 280 | 96 |
| KPI card 1 | 664 | 816 | 400 | 240 |
| KPI card 2 | 1080 | 816 | 400 | 240 |
| KPI card 3 | 1496 | 816 | 400 | 240 |

Proportions: the visual covers 100% of the canvas; the floating panel 28% of the width at
full height; the KPI strip 22% of the height. The callout position moves with the point it
labels.

## Navigation

**Floating icon rail on the left, 64 px.** The reference designs have no navigation; they
are single screens. A report needs one, and on the left it does not cut into the visual's
open area, which is the centre and the right. It floats like the other panels, so the
visual still runs behind it to the edge. Icons, not text: every pixel of panel covers part
of the picture. A top bar is the wrong place here because the filter pills already live
on the top edge.

## What goes in each zone

- **Full-bleed visual** — the map, plan or site, coloured by status. Example: map of
  the solar portfolio, 38 sites, bubble = capacity, colour = output vs forecast.
- **Floating icon rail nav** — one icon per page, current page highlighted.
- **Floating panel** — the narrative and the list. Headline, a short explanation, then
  a ranked list. Example: *"Output is 4% under forecast, driven by 3 sites in the
  north"*, then *Lugo 71% · Burgos 78% · León 83%* of forecast, each with a status dot.
- **Filter pills** — Example: [Today ▾] [All regions ▾] [Solar ▾].
- **Callout** — the one point on the map that needs attention. Example: *Lugo · 71% of
  forecast · inverter fault since 08:15*.
- **KPI cards (3)** — Example: *Output 412 MWh ▼ 4.1% vs forecast* ·
  *Availability 97.2% (target 98%)* · *Revenue today €38.6K ▼ €1.7K vs forecast*.
