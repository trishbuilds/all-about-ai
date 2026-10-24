# all-about-ai: trend pipeline

A daily system for turning AI news, explainers on how AI works, and practical ways of working with AI and agents from X, LinkedIn and other sources into short-video ideas for TikTok, YouTube Shorts and Instagram Reels. About 20 minutes a day from you; Claude does the pulling, merging and scoring.

## Daily flow

| When | Who | What |
| --- | --- | --- |
| On demand | Claude | Say **"pull trends"**: fetches Hacker News, Hugging Face models and Daily Papers, Product Hunt, Simon Willison's blog and GitHub trending, and adds new AI stories to Trend Inbox as **New** with a Pillar. See [prompts/trend-pull.md](prompts/trend-pull.md). |
| Morning, ~3 min | You | Run the three [Grok prompts](prompts/grok-x-search.md), one per pillar, in the X app and paste the answer into the Notion **Drop** page. |
| During the day, ~10 min | You | LinkedIn sweep: save 3 to 5 posts into Drop. See [linkedin/follow-list.md](linkedin/follow-list.md). |
| Any time | You | Note AI tool or agent experiments in the Notion **Lab log**. |
| When ready | You → Claude | Say **"score today"**. Claude merges, kills, scores and shortlists. See [skills/score-trends/SKILL.md](skills/score-trends/SKILL.md). |
| ~5 min | You | Short-video check on the Shortlist (Open / Warm / Crowded), then pick: News today, Evergreen in the Mon/Thu batch. |
| Weekly | You + Claude | Review which videos did best and adjust the [scoring weights](config/scoring.yaml). |

## What's in this repo

| Path | What it is |
| --- | --- |
| [docs/pipeline-overview.md](docs/pipeline-overview.md) | The full strategy: sourcing options, capture, scoring, turning trends into videos, weekly rhythm, costs |
| [docs/pillars.md](docs/pillars.md) | The three content pillars (Trend, How AI works, Working with AI), their sources and weekly mix |
| [docs/daily-workflow.md](docs/daily-workflow.md) | The step-by-step daily gather and filter workflow |
| [docs/tools-and-costs.md](docs/tools-and-costs.md) | Tool options and what each piece costs |
| [prompts/grok-x-search.md](prompts/grok-x-search.md) | Three Grok prompts for the X pull, one per pillar |
| [prompts/claude-scoring.md](prompts/claude-scoring.md) | Prompt to give Claude for manual scoring |
| [config/scoring.yaml](config/scoring.yaml) | Kill rules, scoring weights and the shortlist threshold |
| [linkedin/follow-list.md](linkedin/follow-list.md) | Starter list of LinkedIn people and company pages |
| [notion/workspace.md](notion/workspace.md) | Notion Trend Workspace layout, Trend Inbox schema, Drop and Lab log templates |
| [prompts/trend-pull.md](prompts/trend-pull.md) | The on-demand source pull and its 6 automated sources |
| [skills/pull-trends/SKILL.md](skills/pull-trends/SKILL.md) | The "pull trends" Claude skill |
| [skills/score-trends/SKILL.md](skills/score-trends/SKILL.md) | The "score today" Claude skill |

## Live copies

- Notion [Trend Workspace](https://app.notion.com/p/4022f114d1958164a5aee10da43b9d6c), [Drop](https://app.notion.com/p/4022f114d195814791c4c861f659d1d8) and [Lab log](https://app.notion.com/p/4022f114d1958186a49ee026e4d1faed)
- Doc: [Trend-to-short-video pipeline](https://claude.ai/artifact/JvydwjXBcE1okAAN6YZBLY)
- Doc: [Daily trend gather and filter workflow](https://claude.ai/artifact/6Swh1RzmJpjTW84sXsA8o3)

The live docs and Notion pages are the working copies; this repo is a snapshot taken on 2026-10-23.
