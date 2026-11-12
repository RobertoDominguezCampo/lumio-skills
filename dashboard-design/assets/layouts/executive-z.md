# Layout: Executive Z

KPI strip, one main chart with its context, a detail table. The most common pro pattern
(63 of 301 dashboards, 21%) and the safe default for an executive page.

## When to use it

- **Type of dashboard:** a business watched through a handful of headline numbers.
  Sales, finance, an operations overview, a monthly performance review.
- **Audience:** executives and managers who check the page often and want the verdict
  first, then one level of "why", then the rows to follow up on.
- **Reading path:** a Z. KPIs left to right, down to the main chart, across to its
  context card, then down into the table.

## Grid (1920 × 1080)

```
┌──────┬───────────────────────────────────────────────┐
│      │ Title + filters                               │
│      ├──────────┬──────────┬──────────┬──────────────┤
│ Side │ KPI      │ KPI      │ KPI      │ KPI          │
│ bar  ├──────────┴──────────┴────┬─────┴──────────────┤
│ nav  │ Main chart (the story)   │ Context /          │
│      │                          │ breakdown          │
│      ├──────────────────────────┴────────────────────┤
│      │ Detail table                                  │
└──────┴───────────────────────────────────────────────┘
```

| Zone | x | y | w | h |
|---|---|---|---|---|
| Sidebar nav | 0 | 0 | 320 | 1080 |
| Title + filters | 344 | 24 | 1552 | 64 |
| KPI 1 | 344 | 104 | 376 | 128 |
| KPI 2 | 736 | 104 | 376 | 128 |
| KPI 3 | 1128 | 104 | 376 | 128 |
| KPI 4 | 1520 | 104 | 376 | 128 |
| Main chart | 344 | 248 | 1024 | 440 |
| Context / breakdown | 1384 | 248 | 512 | 440 |
| Detail table | 344 | 704 | 1552 | 352 |

Proportions: sidebar 17% of width · KPI strip 12% of height · main : context = 2 : 1 ·
table 33% of height.

## Navigation

**Text sidebar on the left, 320 px.** Executive reports are usually several pages
(Overview, Sales, Margin, Customers), and executives navigate by page name, so the names
must be readable, not icons. The page is wide enough to pay 17% of the width and still
keep a 1024 px main chart. Putting the navigation on top would take height from the
table, which is already the tightest zone.

## What goes in each zone

- **Sidebar nav**: report name, page list with the current page highlighted, and at the
  bottom the data refresh date. Example: *Overview · Sales · Margin · Customers ·
  Updated 2 Nov 2026*.
- **Title + filters**: page title as a sentence plus the period and 1-2 slicers
  (period, region). Example: *October 2026 · Sales performance* · [Oct 2026 ▾] [All regions ▾].
- **KPI strip (3-5 equal cards, 4 here)**: one number each, with a delta and the
  comparison it is measured against. Example:
  *Net Sales €4.82M ▲ 6.4% vs LY* · *Gross Margin 38.1% ▼ 1.2 pp vs target* ·
  *Orders 12,406 ▲ 3.1%* · *Avg Order Value €388 ▲ 3.2%*.
- **Main chart (the story)**: the trend that explains the KPIs, with a narrative
  headline. Example: *"Sales beat last year in 9 of 10 months; October is the best month
  on record"*, monthly columns 2026 vs a 2025 line, target as a dashed reference.
- **Context / breakdown**: the cut that answers "where": by region, channel or
  category. Example: horizontal bars by region, *North €1.64M · South €1.21M ·
  East €1.08M · West €0.89M*, each with its vs-LY delta.
- **Detail table**: the rows a manager acts on, sorted by deviation. Example: top 10
  products by gap to target, with Sales, Target, Gap and Margin %.

## Variant: Insight (no table)

For presentations and leadership meetings: a short visit, no exploring. Same sidebar,
title and KPI strip; the table goes and both main zones run to the bottom edge.

| Zone | x | y | w | h |
|---|---|---|---|---|
| Main chart or history | 344 | 248 | 1024 | 808 |
| Insight / call to action | 1384 | 248 | 512 | 808 |

### One-page version (no navigation)

Use it when the brief ends in **one action** (see `../brief-template.md`): one page, one
question, no detail table. Filters move into the header, the sidebar goes, and the content
takes the full width.

```
┌──────────────────────────────────────────────────────────────┐
│ Title = the answer, in one sentence        [Store ▾] [Period]│
├──────────────┬──────────────┬──────────────┬─────────────────┤
│ KPI          │ KPI          │ KPI          │ KPI             │
├──────────────┴──────────────┴─────────┬────┴─────────────────┤
│ Main chart (2/3): when / where /      │ Action card (1/3):   │
│ why, with the story marked on it      │ what to do this week │
│                                       │ and what it's worth  │
└───────────────────────────────────────┴──────────────────────┘
```

| Zone | x | y | w | h |
|---|---|---|---|---|
| Header: title + filters | 24 | 24 | 1872 | 64 |
| KPI 1 | 24 | 104 | 456 | 128 |
| KPI 2 | 496 | 104 | 456 | 128 |
| KPI 3 | 968 | 104 | 456 | 128 |
| KPI 4 | 1440 | 104 | 456 | 128 |
| Main chart (2/3) | 24 | 248 | 1240 | 808 |
| Action card (1/3) | 1280 | 248 | 616 | 808 |

- **Navigation:** none. One page needs no menu; the header carries the filters the
  decision needs (store, period) and nothing else.
- **Title:** the answer to the reader's first question, as a sentence, with the key time or
  number in accent.
- **KPI strip:** one card per item the decision is about (product, bike type, team).
  The one that needs action is the selected card; the rest stay neutral.
- **Main chart:** answers *when* (or where) and marks it on the chart: a band, a marker, a
  label. 808 px is tall: pair the chart with a small matrix strip below it when that strip
  helps the same decision.
- **Action card:** the action for this period, the evidence, a small chart that proves it,
  a short checklist, and the money at stake pinned to the bottom.

The insight card holds one message: the finding, why it matters, the next step. Example:
*"South fell 8% short of target in October. Two of its five stores account for 90% of the
gap. Next: review the pricing change from 15 Sep."*
