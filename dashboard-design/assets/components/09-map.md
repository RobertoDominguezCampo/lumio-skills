# Map + top list

**Question it answers:** Where is it happening?

## When to use it
Location matters to the action (where to move bikes).

## When not to
Location doesn't change the decision: use 06.

## Anatomy
- Insight title naming the place in accent
- Metric switch top right
- Map with bubbles sized by volume, coloured by status (red only if bad)
- The selected place with a ring and a dark callout
- Top 5 list next to the map, selected row highlighted, status pill per row

## Size
1024×440. Only sizes from the layout grid.

## Style rules
- Follow the tokens and the quality bar in README.md.
- Title 19 px bold, hero 30 px bold, labels 13 px, axis 11 px. Tabular numbers.
- One accent highlight only. Red only for bad values, green only for on track.
- No empty space: if it doesn't fill the card, use the smaller size.

## In Power BI
Power BI: Azure Maps (bubble layer) + table, cross-highlight between them.

See it in `preview.html`.
