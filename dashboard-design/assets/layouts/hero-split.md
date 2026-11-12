# Layout — Hero Split

One protagonist visual on one side, a two-column card grid on the other. 16 of 301 pro
dashboards (5%), including the Centered Hero variant.

## When to use it

- **Type of dashboard:** one picture carries the answer. A site or store map, a floor
  plan, a production line, a machine, a network. The visual is data, not decoration.
- **Audience:** operations and facility managers, regional leads: people who think in
  places and objects ("which store", "which line") before they think in numbers.
- **Reading path:** the eye lands on the hero first, because it is the largest box. Then
  the KPI band, then the cards, then the table.

## Grid (1920 × 1080)

```
┌──┬──────────────────────────────────────────────────────┐
│  │ Title + filters                                      │
│I ├────────────────────────┬─────────────────────────────┤
│c │                        │ KPI band (3–4 values)       │
│o │  Hero visual           ├──────────────┬──────────────┤
│n │  (map, plan, object)   │ Card         │ Card         │
│  │                        ├──────────────┴──────────────┤
│  │                        │ Detail table                │
└──┴────────────────────────┴─────────────────────────────┘
```

| Zone | x | y | w | h |
|---|---|---|---|---|
| Icon rail nav | 0 | 0 | 80 | 1080 |
| Title + filters | 104 | 24 | 1792 | 64 |
| Hero visual | 104 | 104 | 816 | 952 |
| KPI band | 936 | 104 | 960 | 280 |
| Card 1 | 936 | 400 | 472 | 380 |
| Card 2 | 1424 | 400 | 472 | 380 |
| Detail table | 936 | 796 | 960 | 260 |

Proportions: hero 46% of the content width at full height, cards side 54% as a
two-column grid.

## Navigation

**Icon rail on the left, 80 px.** Most references for this pattern use a top bar
(6 of 7), so this is a deliberate change. A top bar would take 6–10% of the height
from the hero, and a map or a plan is the visual that loses most when it gets shorter.
A rail costs only 4% of the width and leaves the hero at full height. Use icons, not a
text sidebar: a 320 px sidebar would push the hero below 700 px wide.

## What goes in each zone

- **Icon rail nav** — one icon per page, current page highlighted.
- **Title + filters** — Example: *October 2026 · Store network* · [Oct 2026 ▾]
  [All formats ▾].
- **Hero visual** — the map or plan, coloured by status, with a narrative headline.
  Example: *"7 of 42 stores are below target, all of them on the east coast"*. Bubble map,
  bubble size = sales, colour = status vs target. Selecting a store filters the right side.
- **KPI band (3–4 values)** — Example: *Network sales €12.6M ▲ 3.8% vs LY* ·
  *Stores on target 35 / 42* · *Sales per m² €412 ▼ 1.5%* · *Footfall 1.94M ▲ 2.1%*.
- **Card 1** — the "where": Example: sales by region vs target, bullet bars.
- **Card 2** — the "when": Example: weekly sales of the selected store or region, 2026
  vs 2025.
- **Detail table** — stores below target, sorted by gap. Example: *Valencia Centro
  €241K · −11.2% vs target*, with Sales, Target, Gap, Footfall.
