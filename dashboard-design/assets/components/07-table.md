# Table with selectors

**Question it answers:** Which rows need action?

## When to use it
The user has to act on specific rows (stores, products, people).

## When not to
Nobody acts on the rows: summarise with a chart.

## Anatomy
- Insight title with the number of rows to act on in accent
- Selector buttons to switch the grain
- Columns ordered by the decision, bars for %, red only on bad values
- Status badge per row
- The selected row highlighted with an accent edge

## Size
1552×352. Only sizes from the layout grid.

## Style rules
- Follow the tokens and the quality bar in README.md.
- Title 19 px bold, hero 30 px bold, labels 13 px, axis 11 px. Tabular numbers.
- One accent highlight only. Red only for bad values, green only for on track.
- No empty space: if it doesn't fill the card, use the smaller size.

## In Power BI
Power BI: table/matrix with conditional formatting, data bars and field parameters for the selector.

See it in `preview.html`.
