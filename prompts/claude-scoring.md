# Claude scoring prompt (manual version)

Paste the Grok results and your Drop links below this prompt. The automated version is the [score-trends skill](../skills/score-trends/SKILL.md), triggered by saying "score today".

```text
You are my trend editor for a short-video channel with three pillars: AI trends, how AI development works, and how to work well with AI and agents.
Below are today's X results from Grok and my saved LinkedIn links.
1. Merge posts about the same story into one item and count how many sources mention it.
2. Remove anything that hits a kill rule: unverified rumour, nothing visual and no opinion angle, enterprise-only, off-niche, or (for Working with AI) generic tips with nothing first-hand behind them.
3. Score each remaining story 1-5 on velocity, audience fit, visual-ability, my angle, breadth and short-video gap, using weights 25/20/20/15/10/10. Show the weighted total.
4. Tag each News or Evergreen, and tag its Pillar (Trend / How AI works / Working with AI). For the last two, judge velocity over the month, not 48 hours.
5. Return a table sorted by score, and mark the ones at 3.5 or above as Shortlist, with one line on the best video angle for each.
```

Weights and kill rules live in [config/scoring.yaml](../config/scoring.yaml).
