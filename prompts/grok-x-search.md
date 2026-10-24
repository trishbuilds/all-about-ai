# Grok X search prompts (one per pillar)

Run these in Grok (X app or grok.com, free with X Premium) each morning, about 3 minutes, then paste the answers into the Notion **Drop** page under "Grok X results". One prompt per [pillar](../docs/pillars.md) so trend news doesn't crowd out the slower pillars. Grok only searches X, so add Working with AI finds from YouTube, podcasts, blogs and Reddit to Drop by hand.

Automating this through the xAI API costs about $8 a month at one run a day returning ~50 posts (X search is $5 per 1,000 posts returned, plus tokens; checked 2026-10-20 at docs.x.ai/developers/pricing). For now Trish runs it by hand.

```text
TREND: Using X search, list the 10 most-discussed AI launches, demos or controversies from the last 24 hours, with post links and engagement. Skip crypto, giveaways and engagement bait.

HOW AI WORKS: Using X search, find the 5 most-shared posts from AI researchers or lab accounts in the last 3 days that explain a new result, model release or technique. Summarise each in plain English with the link.

WORKING WITH AI: Using X search, find the 8 most-saved or most-shared posts from the last 3 days where people share how they work with AI or agents: their methodology, skills, mindset, workflows, setups, or experiments (including failures and lessons learned). Prefer first-hand accounts over generic tips. Include the link, the author and the one-line takeaway.
```

## Original single prompt (before pillars)

```text
Using X search, find the 30 most-discussed posts about AI and tech from the last 24 hours.
Focus on: new AI models and tools, big product launches, AI in jobs/money/everyday life, viral demos, and controversies.
Skip: crypto, giveaways, engagement bait, and reposts of the same news.
For each, return: topic (5 words), one-line summary, post link, author handle, likes, reposts, and posted time.
Then group posts about the same story and list the 10 biggest stories, ranked by total engagement and how fast it is growing.
```

## X List to scan by hand

AI lab accounts and their founders, a few AI researchers, tool builders who post demos, and 2 to 3 tech news commentators. Keep it under 50 accounts.
