# dashboard-design

This is the skill from my video "Turn Claude into a Senior Power BI Designer in 3 Simple Steps".

Video: link coming soon

## What it does

When you ask Claude for a Power BI dashboard, you normally get a generic page. With this skill, Claude follows the three steps from the video:

1. **Layout.** It picks one of five layout patterns and tells you why.
2. **Components.** It fills every box with a complete component, not a loose visual.
3. **Context.** It asks who the dashboard is for and what they need to decide.

What you get is a design prototype with sample numbers, using only native Power BI visuals. It is the design, not the final report. You build it in Power BI after.

## How to install it

1. Download this repo. Click the green Code button, then Download ZIP.
2. Copy the `dashboard-design` folder.
3. Paste it in `.claude/skills/` inside your project. If you want it in all your projects, paste it in `~/.claude/skills/`.

## How to use it

Just ask for a dashboard design. For example:

> Design a Power BI dashboard for a logistics company.

Claude asks you four questions first: who is it for, what do they decide, what do they ask first, and what the page must never do. Answer them and you get the design.

## What is inside

```
dashboard-design/
  SKILL.md               the rules Claude follows
  assets/
    brief-template.md    the four questions before designing
    layouts/             five layout patterns, with the grid for a 1920 x 1080 page
    components/          ten components, and preview.html to see them
    references/          the quality bar and real pro dashboards
```

The layouts are Executive Z, Main + Insight Rail, Hero Split, List + Canvas and Full-Bleed.

The components are KPI + line, KPI + bar, KPI vs target, Variance bars, Donut + breakdown, Ranking, Table with selectors, Trend comparison, Map + top list and Insight card.

## Colors and fonts

The skill does not decide colors or fonts. Use your own theme or design system. The colors in `assets/components/README.md` are only the ones I used in the preview.

## Where the layouts come from

I looked at 1,081 dashboards and kept the 301 that look professional. The five layouts are the patterns they use the most.

## Credits

The images in `assets/references/` are small thumbnails of dashboards published on Tableau Public. Each one has its author and its link in [`assets/references/README.md`](assets/references/README.md). They belong to their authors. I only use them as a reference. If one is yours and you want it out, open an issue and I will remove it.
