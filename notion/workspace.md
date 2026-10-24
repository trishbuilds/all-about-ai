# Notion Trend Workspace

Created 2026-10-23 as a private top-level page.

```text
📈 Trend Workspace          https://app.notion.com/p/4022f114d1958164a5aee10da43b9d6c
├── Three pillars, daily routine, Grok prompts, scoring prompt, kill rules, weights (page body)
├── Trend Inbox (database)  https://app.notion.com/p/fc9fc1644e91453b9ebf452413281657
│                           data source: collection://44f83f57-1f13-456d-afb7-f686301c91b0
├── 📥 Drop (page)          https://app.notion.com/p/4022f114d195814791c4c861f659d1d8
└── 🧪 Lab log (page)       https://app.notion.com/p/4022f114d1958186a49ee026e4d1faed
```

## Trend Inbox schema

One row per story, not per post.

| Property | Type | Values / notes |
| --- | --- | --- |
| Topic | title | 5-word name of the story |
| Summary | text | One line on what happened |
| Sources | text | All post links, " · " separated (name + points/likes + link) |
| Sources count | number | How many independent sources |
| Platform | multi-select | X, LinkedIn, Other |
| Pillar | select | Trend, How AI works, Working with AI |
| First seen | date | |
| Short-video check | select | Open, Warm, Crowded |
| Score | number | Weighted total out of 5 |
| Type | select | News, Evergreen |
| Status | status | To do: New (default) · In progress: Shortlist, Scripted, Filmed · Complete: Posted, Killed |
| Best angle | text | One line from Claude |

**Board view:** grouped by Status, sorted by Score descending within each column.

## Drop page template

```markdown
Paste raw finds here during the day: Grok's answer and LinkedIn links, each with one line on why it caught your eye. Clear it after each scoring run.

## Grok X results

## LinkedIn saves
- [link] — why it caught my eye

## Other (HN, Reddit, anything else)
- [link] — why
```

## Lab log page template

Jot down every time an AI tool or agent surprised you, failed, or saved you time. One line is enough. These become "I tested it" and Working-with-AI videos.

| Date | Tool / agent | What I tried | What happened | Video idea? |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
