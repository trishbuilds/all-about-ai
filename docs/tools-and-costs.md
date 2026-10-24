# Tools and costs

Gathered 2026-10-20 to 2026-10-23. Only the xAI price was checked against a live pricing page; the rest are from memory, so check before paying.

## Recommended starting setup (~$10/month)

1. **Grok with X search** for the daily X pull (manual in the X app for now, free with X Premium).
2. **LinkedIn by hand:** save 3 to 5 posts a day into Notion.
3. **TikTok Creative Center (free)** to check what's already hot on short video.
4. **Claude** scores the trends and drafts idea cards with hooks and scripts.
5. **CapCut (free)** for editing.

Hold off on Taplio and Tweet Hunter until LinkedIn or X proves to be your best source.

## Running costs

| Piece | Tool | Cost |
| --- | --- | --- |
| Inbox and idea board | Notion | Free plan is enough |
| Automated X signal | xAI API with X search | ~$8/month at one run a day returning ~50 posts; ~$30-35/month at ~200 posts. X search is $5 per 1,000 posts returned (quoted/parent posts count), plus grok-4.3 tokens at $1.25/M in and $2.50/M out. Prepaid credit; no free starter credit mentioned. Checked 2026-10-20 at https://docs.x.ai/developers/pricing |
| Other sources | HN, GitHub, Hugging Face, Product Hunt, TikTok Creative Center | Free |
| Pulling, scoring, scripting | Claude (on demand) | Included in the Claude plan |
| Editing | CapCut | Free; Pro ~$8-20/month |
| Scheduling posts | Native apps, Buffer, Metricool | Free tiers available |
| Official X API | Basic tier | ~$200/month. Not needed. |

## Using Grok from a terminal

X Premium only covers Grok in the X app and grok.com. For scripts, create a pay-as-you-go account at console.x.ai, add credit ($5 is plenty to start), create an API key, then call `https://api.x.ai/v1` (OpenAI-compatible) or use the Python SDK (`pip install xai-sdk`) with the X search tool turned on.

## Other tools considered

| Need | Tool | Notes |
| --- | --- | --- |
| X / LinkedIn trends | Taplio | Searchable library of viral LinkedIn posts. ~$40-65/month |
| X trends | Tweet Hunter | ~$50/month |
| Topic tracking | Feedly AI | News, blogs, Reddit; daily summary; free tier |
| Rising topics | Exploding Topics | Better for longer trends than daily news |
| Short-video check | TikTok Creative Center | Trending hashtags, sounds, top ads; free |
| Short-video check | vidIQ | YouTube/Shorts trends, AI ideas and titles; free tier |
| Editing | CapCut | Editing, auto-captions, templates |
| Repurposing | Opus Clip | Cuts long recordings into Shorts |
