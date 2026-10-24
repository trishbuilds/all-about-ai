# Trend pull (on demand)

- **Run:** on demand. Say "pull trends" to Claude; the [pull-trends skill](../skills/pull-trends/SKILL.md) has the full steps. A daily 06:45 UTC scheduled run existed on 2026-10-23 but was removed the same day at Trish's request.
- **Writes to:** Notion Trend Inbox (`collection://44f83f57-1f13-456d-afb7-f686301c91b0`), as New rows tagged with a Pillar
- **Cost:** nothing beyond the Claude plan

The pull only gathers. It does not score or shortlist; that happens when Trish says "score today".

## Automated sources

| Source | URL fetched | Mostly feeds |
| --- | --- | --- |
| Hacker News front page | https://hn.algolia.com/api/v1/search?tags=front_page&hitsPerPage=40 | Trend, How AI works |
| Hugging Face trending models | https://huggingface.co/api/models?sort=trendingScore&limit=15 | Trend |
| Hugging Face Daily Papers | https://huggingface.co/api/daily_papers?limit=15 | How AI works |
| Product Hunt | https://www.producthunt.com/feed | Trend, Working with AI |
| Simon Willison's blog (last 3 days) | https://simonwillison.net/atom/everything/ | Working with AI, How AI works |
| GitHub trending (daily) | https://github.com/trending?since=daily | Working with AI (often nothing useful) |

Not automatable: Reddit (blocks automated access), LinkedIn, TikTok Creative Center. X comes from the [Grok prompts](grok-x-search.md).
