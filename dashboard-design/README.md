# dashboard-design

The skill from the Lumio Visuals video **"Turn Claude into a Senior Power BI Designer in 3 Simple Steps"**.

It makes Claude design a Power BI dashboard page the way a senior designer would, before anything is built in Power BI:

1. **Layout** — it picks one of five layout patterns and tells you why.
2. **Components** — it fills every zone with a closed component, never a loose visual.
3. **Context** — it starts from a brief: audience, decision, first question, never.

The output is a design prototype with realistic sample numbers, native Power BI visuals only, plus a senior review and a handoff for the build.

Video: _link coming soon_

## Install

**Claude Code**

Download this repo and copy the `dashboard-design` folder into your skills folder:

- One project: `<your-project>/.claude/skills/dashboard-design/`
- All your projects: `~/.claude/skills/dashboard-design/`

**Claude app**

Zip the `dashboard-design` folder and add it as a custom skill.

## Use it

Ask for a dashboard design in plain words:

> Design a dashboard page for the fleet manager of a bike rental store. Every week she decides which bikes to have ready so nothing sells out at peak hours.

If you give no brief, Claude asks the four brief questions first.

## What is inside

```
dashboard-design/
├── SKILL.md                  the rules Claude follows
├── README.md                 this file
└── assets/
    ├── brief-template.md     the four questions to ask before designing
    ├── layouts/              five layout patterns, with a pixel grid for 1920 × 1080
    ├── components/           ten components + preview.html to see them
    └── references/           the quality bar and real pro dashboards
```

- **Layouts:** Executive Z, Main + Insight Rail, Hero Split, List + Canvas, Full-Bleed.
- **Components:** KPI + line, KPI + bar, KPI vs target, Variance bars, Donut + breakdown, Ranking, Table with selectors, Trend comparison, Map + top list, Insight card.
- **Colours and fonts** are not part of this skill. Bring your own design system or Power BI theme. The tokens in `assets/components/README.md` are only the ones used in the preview.

## Where the patterns come from

The grids and shares come from a study of 1,081 dashboards, of which 301 were kept as pro level.

## Credits

The reference images in `assets/references/` are small thumbnails of dashboards published on Tableau Public. Each one is credited and linked to its author in [`assets/references/README.md`](assets/references/README.md). They belong to their authors and are here for reference only. If one is yours and you want it removed, open an issue.

Everything else is by [Lumio Visuals](https://www.youtube.com/channel/UCMoV2ElmrXMxX_NzrGXCdJA).
