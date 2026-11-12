# dashboard-design

A Claude skill to design Power BI dashboards and reports that look professional.

## What it is

It is a design skill. You tell Claude what dashboard you need and Claude makes a prototype of the page: the layout, the components and the story it tells.

It does not create the Power BI file. That is on purpose. First you get the design right, and then you build it in Power BI. Changing a prototype takes one minute. Changing a finished report takes a lot more.

With every design you also get a handoff: the measures and the native Power BI visual you need for each part of the page. So when you go to Power BI, you already know what to build.

## What you need

- Claude Code. That is where I use it.
- Nothing else to start. You don't need Power BI open and you don't need real data. The prototype uses sample numbers.
- Power BI Desktop later, when you build the report.

## How to install it

1. Download this repo. Click the green Code button, then Download ZIP.
2. Copy the `dashboard-design` folder.
3. Paste it in `.claude/skills/` inside your project. If you want it in all your projects, paste it in `~/.claude/skills/`.

## How to use it

1. Ask Claude for a dashboard design.
2. Claude asks you four questions: who is it for, what do they decide with it, what do they ask first, and what the page must never do.
3. Claude picks a layout, tells you why, and makes the prototype. It is usually an HTML page you open in your browser.
4. Look at it and ask for changes, like you would do with a designer.
5. When you like it, use the handoff to build it in Power BI.

## Examples

The simple way. Claude will ask you the questions:

> Design a Power BI dashboard for a logistics company.

With the context from the start. This gives you the best result:

> Design a Power BI dashboard page.
> Audience: the transport manager.
> Decision: every morning, which routes and carriers to act on so deliveries arrive on time.
> First question they ask: which deliveries will be late today, and why?
> Never: show numbers they can't act on.

When you only want to decide the structure:

> I need a monthly sales page for the leadership team. Which layout would you use, and why?

When you want to change something:

> I like it, but the ranking has to stay visible all the time. Try another layout.

## How to get more out of it

- Be specific with the audience. "The fleet manager of one store" works much better than "management".
- Always say what the page must never do. It is the fastest way to remove things that say nothing.
- If you don't like the layout, ask for another one of the five and ask why. The reason helps you decide.
- The components are a starting point. Ask Claude to adapt them to your data and your question.
- The skill does not decide colors or fonts. Give Claude your theme or your design system and it will use it.
- Open `assets/components/preview.html` in your browser to see the ten components before you start.

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

The layouts come from real dashboards. I looked at 1,081 and kept the 301 that look professional. The five layouts are the patterns they use the most.

## The video

I build this skill step by step in "Turn Claude into a Senior Power BI Designer in 3 Simple Steps". Link coming soon.

## Credits

The images in `assets/references/` are small thumbnails of dashboards published on Tableau Public. Each one has its author and its link in [`assets/references/README.md`](assets/references/README.md). They belong to their authors. I only use them as a reference. If one is yours and you want it out, open an issue and I will remove it.
