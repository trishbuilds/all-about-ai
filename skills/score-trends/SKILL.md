---
name: score-trends
description: Use when Trish says "score today" or asks to score, filter or shortlist trends in her Notion Trend Inbox for short-video ideas.
---

# Score today's trends

Turn the day's raw finds into a scored shortlist of short-video ideas (TikTok, YouTube Shorts, Instagram Reels) for Trish's AI channel.

## The channel's three pillars
Every story must fit one pillar; tag it in the Pillar field.
- **Trend**: what's happening in AI now: launches, viral demos, controversies, big company moves. Shelf life 24-48h.
- **How AI works**: how AI development works: research results, model releases explained, why something works or fails (agents, reasoning, context, benchmarks). Shelf life weeks.
- **Working with AI**: how people actually work with AI and agents: their methodology, skills, mindset, workflows, setups and experiments (what worked, what failed, lessons learned), shared on X, LinkedIn, YouTube, podcasts, blogs, Reddit or anywhere else. Trish's own experiments (Lab log) count and are the strongest source. Prefer first-hand accounts over generic tips. Shelf life weeks to months.

Weekly mix to aim for: about 3 Trend, 2 How AI works, 2 Working with AI.

## Where things live (Notion)
- **Trend Workspace** page: https://app.notion.com/p/4022f114d1958164a5aee10da43b9d6c
- **Trend Inbox** database, data source `collection://44f83f57-1f13-456d-afb7-f686301c91b0`. Fields: Topic, Summary, Sources, Sources count, Platform (X / LinkedIn / Other), Pillar (Trend / How AI works / Working with AI), Short-video check (Open / Warm / Crowded), Score, Type (News / Evergreen), Status (New, Shortlist, Scripted, Filmed, Posted, Killed), Best angle, First seen.
- **Drop** page: https://app.notion.com/p/4022f114d195814791c4c861f659d1d8 . Trish pastes Grok X results (one section per pillar), LinkedIn links and finds from other platforms here.
- **Lab log** page: https://app.notion.com/p/4022f114d1958186a49ee026e4d1faed . Trish's own AI/agent experiments. Rows added since the last scoring run become Working with AI stories.

## Steps
1. Read all Trend Inbox rows with Status = New, the Drop page, and new Lab log rows.
2. Turn each Drop item and new Lab log row into a story. Merge items about the same story across platforms into one row: combine Sources (" · " separated), set Sources count, and set Platform to every platform it came from. Create rows for stories not already in the Inbox; update existing rows rather than duplicating.
3. Tag Pillar on every story (fill it in for any New row missing one).
4. Kill (Status = Killed) any story that hits a kill rule:
   - rumour from a single anonymous source, or unverifiable
   - nothing to show on screen and no strong opinion or lesson to share
   - enterprise-only news with no effect on everyday people or individual practitioners
   - Short-video check is Crowded and there's no contrarian angle
   - doesn't fit any of the three pillars
   - Working with AI: generic, recycled tips with no first-hand method, experiment or result behind them
5. Score each survivor 1-5 on each criterion, then compute the weighted total (one decimal) into Score:
   | Criterion | Weight | A 5 looks like |
   | --- | --- | --- |
   | Velocity | 25% | Trend: took off in the last 24-48h and still climbing. How AI works / Working with AI: getting real attention this month |
   | Audience fit | 20% | Viewers would use it, feel it, or change how they work with AI this week |
   | Visual-ability | 20% | Can be shown on screen in under 10 seconds (demo, before/after, screen recording of the workflow) |
   | Your angle | 15% | Room for a test, a take or a fresh explanation. Working with AI: Trish can try the method herself before filming (her own Lab log experiments score 5) |
   | Breadth | 10% | On X and LinkedIn, or 3+ sources |
   | Short-video gap | 10% | Open on TikTok/Shorts (use 3 if not yet checked) |
6. Set Type: News (must be posted within 48h) or Evergreen. Trend is usually News; the other two pillars are usually Evergreen.
7. Score >= 3.5 -> Status = Shortlist and write Best angle: one line naming the angle (I tested it, what it means for you, how to use it, myth vs reality, hot take, explain it simply, comparison, behind the method) and the concrete video. Below 3.5 -> leave as New if it is less than 3 days old (Trend) or 14 days old (other pillars), otherwise Killed.
8. Clear the Drop page back to its empty template (headings: Grok X results, LinkedIn saves, Other) once everything is in the Inbox. Never clear the Lab log.
9. Reply briefly: how many scored, killed and shortlisted; the shortlist as a short list (topic, pillar, score, News/Evergreen, best angle), News first; and a one-line pillar balance check against the 3/2/2 weekly mix (count Shortlist + Scripted + Filmed + Posted from the last 7 days), naming any pillar running thin. Remind Trish to do the 5-minute TikTok/Shorts check (Open / Warm / Crowded) on the shortlist.

## Rules
- Never delete Inbox rows; use Status = Killed.
- Don't touch rows already at Scripted, Filmed or Posted.
- Adjust weights only when Trish asks, or after the weekly review she requests.
