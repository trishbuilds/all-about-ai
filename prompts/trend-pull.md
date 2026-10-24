# Trend pull (on demand)

- **Run:** on demand. Ask Claude to "pull trends" (or paste the prompt below) in the project. A daily 06:45 UTC scheduled run existed from 2026-10-23 but was removed the same day at Trish's request.
- **Writes to:** Notion Trend Inbox (`collection://44f83f57-1f13-456d-afb7-f686301c91b0`)
- **Cost:** nothing beyond the Claude plan

## Sources

| Source | URL | Status |
| --- | --- | --- |
| Hacker News front page | https://hn.algolia.com/api/v1/search?tags=front_page&hitsPerPage=30 | Works |
| Hugging Face trending models | https://huggingface.co/api/models?sort=trendingScore&limit=15 | Works |
| GitHub trending (daily) | https://github.com/trending?since=daily | Works |
| Product Hunt | https://www.producthunt.com/feed | Works |
| Reddit | r/OpenAI, r/LocalLLaMA, r/ChatGPT… | Blocked for automated access; paste good finds into Drop instead |
| TikTok Creative Center | — | No API; stays a manual 5-minute check |

The pull only gathers. It does not score or shortlist; that happens when Trish says "score today".

## Prompt

```text
Trend pull for Trish. Do it end to end without asking questions, same as the Oct 23 test run:
1. WebFetch (curl is blocked; Reddit is blocked, skip it): https://hn.algolia.com/api/v1/search?tags=front_page&hitsPerPage=30 · https://huggingface.co/api/models?sort=trendingScore&limit=15 · https://github.com/trending?since=daily · https://www.producthunt.com/feed
2. Keep only AI/tech items an everyday short-video audience would care about; drop dev-infra, security minutiae and non-AI items.
3. Merge items about the same story and count sources.
4. Query Trend Inbox (collection://44f83f57-1f13-456d-afb7-f686301c91b0) and skip stories already added in the last 7 days.
5. Add the top 10 new stories: Topic, Summary, Sources (name + points/likes + link, " · " separated), Sources count, Platform = Other, Status = New, First seen = today. Leave Score, Type, Short-video check, Best angle empty.
6. Post one short line in the thread listing the count and 2-3 standout topics. Don't score, shortlist or delete anything. If Notion or the sources fail, say what failed in one line.
```
