# Daily trend gather and filter workflow

Snapshot of the [live doc](https://claude.ai/artifact/6Swh1RzmJpjTW84sXsA8o3), written 2026-10-23.

The daily routine takes about 20 minutes of your time and ends with 3 to 5 scored stories ready to script. Grok and Claude do the pulling and scoring; you add LinkedIn and make the final call. Everything lands in one Notion database, Trend Inbox, one row per story.

1. **Grok X pull (you, ~3 min):** three Grok prompts, one per [pillar](pillars.md).
2. **LinkedIn sweep (you, 10 min):** save 3 to 5 posts to the Notion Drop page.
3. **Merge (Claude):** combine both lists with the on-demand source pull, group posts about the same story, count sources.
4. **Short-video check (you or Claude, 5 min):** look up the top topics in TikTok Creative Center and on YouTube Shorts.
5. **Score and kill (Claude):** apply the kill rules, score what's left, tag News or Evergreen.
6. **Lab log (any time):** note any AI tool or agent that surprised you, failed or saved you time.
7. **Pick (you, 5 min):** choose which shortlisted stories to make today; News first.

## Step 1: Grok X pull

One Grok call a day with X search, capped at about 50 posts, costs roughly $8 a month through the API. For now, paste the prompts into Grok in the X app for free. Prompts: [prompts/grok-x-search.md](../prompts/grok-x-search.md).

## Step 2: LinkedIn sweep

LinkedIn has no API you can use, so this step is 10 minutes by hand. It's where you find the business and career angle that X misses. Steps and the starter follow list: [linkedin/follow-list.md](../linkedin/follow-list.md).

## Step 3: Short-video check

For each of the top 10 stories, spend 30 seconds checking whether short-video audiences have caught on yet. You want stories hot on X or LinkedIn but still thin on TikTok and Shorts.

- **TikTok:** search the topic and filter to the last week. Note how many videos there are and their view counts.
- **TikTok Creative Center:** check whether a related hashtag is rising, and note any trending sound you could use.
- **YouTube Shorts:** search the topic and look at upload dates.

Rate it: **Open** (under ~5 decent videos), **Warm** (some coverage, room for a fresh angle) or **Crowded** (big creators have covered it). This feeds the "Short-video gap" score.

## Step 4: Filter and score

First kill anything that fails a hard rule, then score the rest. Only stories scoring 3.5 or higher make the shortlist. Rules and weights: [config/scoring.yaml](../config/scoring.yaml). Prompt: [prompts/claude-scoring.md](../prompts/claude-scoring.md), or say "score today" to use the [score-trends skill](../skills/score-trends/SKILL.md).

Tag each survivor with its Pillar, and **News** (post within 48h or drop it) or **Evergreen** (can wait in the backlog).

## Output

Each day ends with one updated Trend Inbox in Notion and 3 to 5 shortlisted stories you can hand straight to scripting. Field list: [notion/workspace.md](../notion/workspace.md).

Pick from the Shortlist each day: film News items the same day, and move Evergreen ones to your Monday/Thursday batch. Once a week, look at which posted videos did best and adjust the weights.
