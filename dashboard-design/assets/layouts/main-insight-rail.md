# Layout — Main + Insight Rail

An analysis column on the left with a full-height rail of status, rankings and alerts on
the right. 24 of 301 pro dashboards (8%).

## When to use it

- **Type of dashboard:** a ranking, an alert or a status has to stay in view while the
  user works through the main analysis. Sales with top products, operations with open
  alerts, service desks with SLA breaches.
- **Audience:** managers and analysts who spend time on the page and come back to it
  during the day. They work down the main column and glance at the rail at any moment.
- **Reading path:** the main column top to bottom. The rail is read like a margin of
  findings, at any time.

## Grid (1920 × 1080)

```
┌──┬────────────────────────────────────┬──────────────────┐
│  │ Title + filters                    │ Status / alert   │
│  ├────────┬────────┬────────┬─────────┤                  │
│I │ KPI    │ KPI    │ KPI    │ KPI     ├──────────────────┤
│c ├────────┴────────┴────────┴─────────┤ Top N ranking    │
│o │ Main chart (the story)             │                  │
│n │                                    ├──────────────────┤
│  ├────────────────────────────────────┤ Secondary        │
│  │ Detail table                       │ breakdown        │
└──┴────────────────────────────────────┴──────────────────┘
```

| Zone | x | y | w | h |
|---|---|---|---|---|
| Icon rail nav | 0 | 0 | 80 | 1080 |
| Title + filters | 104 | 24 | 1216 | 64 |
| KPI 1 | 104 | 104 | 292 | 128 |
| KPI 2 | 412 | 104 | 292 | 128 |
| KPI 3 | 720 | 104 | 292 | 128 |
| KPI 4 | 1028 | 104 | 292 | 128 |
| Main chart | 104 | 248 | 1216 | 400 |
| Detail table | 104 | 664 | 1216 | 392 |
| Rail — status / alert | 1336 | 24 | 560 | 320 |
| Rail — Top N ranking | 1336 | 360 | 560 | 376 |
| Rail — secondary breakdown | 1336 | 752 | 560 | 304 |

Proportions: main column 68% of the content width, rail 31%, rail at full height.

## Navigation

**Icon rail on the left, 80 px.** This page already has two columns. A 320 px text
sidebar would squeeze the main column below 1000 px and the rail below 500 px, and both
need their width. Icons are enough because these users visit the report daily and know
the pages. Navigation on the left keeps the right edge for the rail, which must reach
the top of the page to stay visible.

## What goes in each zone

- **Icon rail nav** — one icon per page with a tooltip, current page highlighted.
- **Title + filters** — over the main column only; the rail starts at the top. Example:
  *Week 44 · Order fulfilment* · [Last 7 days ▾] [All warehouses ▾].
- **KPI strip (4 cards)** — Example: *Orders shipped 18,240 ▲ 4.2% vs last week* ·
  *On-time rate 94.6% ▼ 0.8 pp vs 96% target* · *Avg lead time 2.3 days* ·
  *Backlog 1,128 orders ▲ 14%*.
- **Main chart** — daily trend with a narrative headline. Example: *"On-time rate
  dropped below target on Thursday and has not recovered"*, line of on-time % with the
  96% target dashed.
- **Detail table** — the items behind the trend. Example: late orders by customer, with
  Orders, Late, Late %, Days late.
- **Rail — status / alert (top)** — the most urgent thing on the page, always first.
  Example: *3 open alerts · Madrid DC at 81% on-time (target 96%)*, red status dot.
- **Rail — Top N ranking** — Example: top 5 warehouses by backlog, *Madrid 412 ·
  Valencia 268 · Sevilla 190 · Bilbao 141 · Zaragoza 117*.
- **Rail — secondary breakdown** — Example: late orders by cause, *Carrier 46% ·
  Stock-out 31% · Picking 23%*.
