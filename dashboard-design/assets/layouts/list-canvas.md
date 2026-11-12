# Layout — List + Canvas

Master-detail: pick an item in the list on the left, the canvas answers about it on the
right. 16 of 301 pro dashboards (5%).

## When to use it

- **Type of dashboard:** operational tracking of single things. Shipments, orders,
  tickets, projects, assets, accounts.
- **Audience:** operators, coordinators and account managers who work item by item.
  They come with a question about one thing ("where is order 48213?"), not about the
  total.
- **Reading path:** the list says *what*, the canvas says *where* or *how*, the bottom
  cards give the detail of the selected item.

## Grid (1920 × 1080)

```
┌──┬──────────────────────────────────────────────────────┐
│  │ Title + filters                                      │
│I ├────────────────┬─────────────────────────────────────┤
│c │ Search         │                                     │
│o │ ▣ Item (sel.)  │ Canvas (map, route, timeline, plan) │
│n │ □ Item         │                                     │
│  │ □ Item         ├──────────────────┬──────────────────┤
│  │ □ Item         │ Detail           │ Detail           │
│  │ □ Item         │                  │                  │
└──┴────────────────┴──────────────────┴──────────────────┘
```

| Zone | x | y | w | h |
|---|---|---|---|---|
| Icon rail nav | 0 | 0 | 80 | 1080 |
| Title + filters | 104 | 24 | 1792 | 64 |
| Item list (container) | 104 | 104 | 544 | 952 |
| Search / slicer | 120 | 160 | 512 | 48 |
| Item 1 (selected) | 120 | 224 | 512 | 152 |
| Item 2 | 120 | 388 | 512 | 152 |
| Item 3 | 120 | 552 | 512 | 152 |
| Item 4 | 120 | 716 | 512 | 152 |
| Item 5 | 120 | 880 | 512 | 152 |
| Canvas | 664 | 104 | 1232 | 560 |
| Detail 1 | 664 | 680 | 608 | 376 |
| Detail 2 | 1288 | 680 | 608 | 376 |

Proportions: list 30% of the content width, canvas 69%; the canvas takes the top 52% of
the height.

## Navigation

**Icon rail on the left, 80 px.** The list is already a left column. A text sidebar next
to it would put two menus side by side, and the user could not tell which one picks the
page and which one picks the item. A thin icon rail keeps the page menu small and clearly
separate. It also leaves the canvas above 1200 px wide, which a map or route needs.

## What goes in each zone

- **Icon rail nav** — one icon per page, current page highlighted.
- **Title + filters** — Example: *Live shipments · 214 in transit* · [Today ▾]
  [All carriers ▾] [Delayed only ☐].
- **Search / slicer** — search by ID or customer, and a status filter.
- **Item cards (list)** — one card per item, sorted by urgency, selected one highlighted.
  Each shows ID, name, status badge and one key number. Example:
  *SHP-48213 · Iberia Foods · Delayed 6 h · ETA 18:40* ·
  *SHP-48197 · Norte Retail · On time · ETA 14:10*.
- **Canvas** — where the selected item is. Example: route map Valencia → Madrid, current
  position, planned vs actual path, with the headline *"SHP-48213 is 6 h late, held at
  the Albacete hub since 09:20"*.
- **Detail 1** — the item's history. Example: timeline of events, *Picked 06:05 ·
  Loaded 07:30 · Hub arrival 09:20 · Hub departure —*.
- **Detail 2** — the item's figures vs plan. Example: *Value €18,450 · 24 pallets ·
  Promised 12:40 · New ETA 18:40 · Penalty risk €920*.
