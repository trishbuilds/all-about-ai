# Trend-to-short-video pipeline (X + LinkedIn → TikTok/Shorts/Reels)

Snapshot of the [live doc](https://claude.ai/artifact/JvydwjXBcE1okAAN6YZBLY), written 2026-10-20.

## TL;DR

The workable setup for a solo creator is: let automation pull from sources with friendly APIs, add X and LinkedIn through a light manual "save" habit plus one legit X search route, then have Claude score everything and draft video ideas into one Notion board each morning. Full automation on X is expensive and on LinkedIn it is against the rules, so don't build the system around scraping them.

1. **Source:** pull trends daily from X (Lists + a search API), LinkedIn (manual saves), and cross-check sources like Hacker News, Reddit, GitHub and TikTok Creative Center.
2. **Capture:** everything lands in one inbox (a Notion database), clustered so the same story from five places becomes one row.
3. **Score:** rate each trend on velocity, breadth, visual-ability, audience fit, your angle and shelf life; kill anything below the bar.
4. **Shape:** turn the top 3 to 5 into idea cards: hook, angle, format, 30-45s beat sheet, platform tweaks.
5. **Ship and learn:** batch-film twice a week, then feed retention and share numbers back into the scoring weights.

## 1. Sourcing: what's actually possible

X can be automated if you pay or go through Grok; LinkedIn realistically cannot, so treat it as a 10-minute manual habit. Pricing is approximate; check it before signing up for anything.

| Source | Automated access | Realistic setup |
| --- | --- | --- |
| X (official API) | Free tier is basically write-only. Basic is roughly $200/mo for a small monthly read quota; Pro is about $5,000/mo. X has also been trialling pay-per-use pricing. | Only worth it once the channel earns money. |
| X via Grok / xAI API | Grok's X search returns recent posts and summaries legitimately. | Best automated route: a daily query like "most-discussed AI tools and launches on X in the last 24h, with post links and engagement". |
| X manually | Lists, Communities, bookmarks, X Pro (TweetDeck, needs Premium). | Build 2 to 3 Lists (AI labs + researchers, AI builders/tool makers, tech commentators). Bookmark anything that pops. |
| X scrapers (Apify etc.) | Works, but breaks X's terms. | Avoid on your main account; accounts and IPs get banned. |
| LinkedIn | No API for reading the feed or searching posts. Partner APIs only cover pages you manage. Scraping breaks the User Agreement and LinkedIn bans fast. | Follow 30 to 50 AI/tech voices, sort feed by recent, check LinkedIn News, and save posts. LinkedIn is best for business-angle stories ("how companies use AI", layoffs, hiring). |
| Hacker News | Free Algolia API, no key. | Fully automatable. Great early signal for dev/AI launches. |
| Reddit | Free API with limits. | r/LocalLLaMA, r/OpenAI, r/ChatGPT, r/singularity, r/artificial. (Blocks automated access from Claude as of 2026-10-23.) |
| GitHub, Hugging Face, Product Hunt | Trending pages and public APIs. | New repos, models and tools you can demo on screen. |
| TikTok Creative Center, YouTube search, Google Trends | Public web pages. | Check whether a topic is already hot on short-video, and which sounds/hashtags are rising. |

The key idea: X and LinkedIn tell you what the tech crowd is talking about; HN, Reddit and GitHub confirm it independently; TikTok Creative Center and YouTube tell you whether short-video audiences have caught on yet. The sweet spot is a topic hot in the first group but not yet saturated in the last.

## 2. Capture and dedupe into one inbox

Everything goes into a single Notion database called Trend Inbox, one row per story, not per post. See [notion/workspace.md](../notion/workspace.md).

- **Manual drops:** when you save something on X or LinkedIn, paste the link into the "Drop" page in Notion. Claude processes it on the next scoring run.
- **Automated pulls:** saying "pull trends" adds stories from HN, Hugging Face (models and Daily Papers), Product Hunt, Simon Willison's blog and GitHub trending. See [prompts/trend-pull.md](../prompts/trend-pull.md).
- **Dedupe:** Claude clusters rows about the same thing (e.g. a model launch that shows up on X, HN and Reddit) into one row and lists every source link on it. The number of sources becomes your breadth signal.

## 3. Filter and score

Score each story 1 to 5 on six criteria, multiply by the weight, and only shortlist stories scoring 3.5 or higher. Weights and kill rules: [config/scoring.yaml](../config/scoring.yaml). Adjust them after a month of real results.

Also tag each story **News** (post within 24 to 48h or skip) or **Evergreen** (can sit in the backlog). That tag decides what you film first.

## 4. Turn trends into video ideas

One trend should become two or three different videos, each picking a different angle. Pick the angle first, then the format, then write the hook last.

**Angles that work for tech/AI**

| Angle | Example on a new AI tool launch |
| --- | --- |
| I tested it | "I gave this new model my real work for a day" |
| What it means for you | "This update changes how you'll search Google" |
| How to use it | "3 ways to use it before everyone else does" |
| Myth vs reality | "Everyone on X says it replaces designers. Here's what it actually did" |
| Hot take | "This is the most overhyped launch of the year, and here's why" |
| Explain it simply | "What an AI agent actually is, in 30 seconds" |
| Comparison | "Same prompt, three tools, one clear winner" |

**Formats**

- **Screen-record demo** with your face in a corner: best for tools.
- **Green-screen over the post or headline** (credit the author on screen): best for news and takes.
- **Talking head + b-roll:** best for explainers and opinions.
- **Side-by-side split:** best for comparisons and before/after.
- **Carousel** (Instagram and TikTok photo mode): best for lists and "5 tools" posts; cheap to make.

**Hook templates** (first 1 to 2 seconds, said out loud and shown as text)

- "Everyone on X is freaking out about [thing]. Here's what's real."
- "[Big company] just quietly [did thing], and it affects you."
- "Stop using [old tool]. This does it in 10 seconds."
- "I tried [viral thing] so you don't have to."
- Start mid-action: open on the wildest output, then explain.

**Beat sheet for a 30 to 45 second video:** hook (0 to 2s) → context in one line (2 to 6s) → proof on screen (6 to 30s) → your take or the "so what" (30 to 40s) → a soft CTA like "follow for the next one" or a question for comments.

**Platform tweaks**

| Platform | Tweak |
| --- | --- |
| TikTok | Keyword-rich on-screen text and caption (TikTok search matters), a rising sound from Creative Center at low volume, 20 to 45s |
| YouTube Shorts | Searchable title, clean audio, no TikTok watermark; slightly longer explainers (up to 3 min) are fine |
| Instagram Reels | Strong cover frame, post the carousel version too, collab tag when you feature another creator |

**The idea card Claude drafts for each shortlisted story:** trend + source links · why now · angle · format · 3 hook options · beat-sheet script · on-screen text · b-roll/screens to capture · caption + hashtags per platform · News or Evergreen.

Copyright note: showing a screenshot of a public post with credit and your own commentary is normal practice; re-uploading someone else's video clip is not.

## 5. Weekly rhythm

| When | Who | What |
| --- | --- | --- |
| On demand | Claude | Pull HN, GitHub, HF, Product Hunt into Trend Inbox when you say "pull trends" |
| Daily, 10 to 15 min | You | Grok X pull, LinkedIn sweep, drop 3 to 5 links into Notion, say "score today", pick which ideas to make |
| Same day | You | Film any News items that scored high (they expire in 24 to 48h) |
| Mon and Thu | You | Batch-film 3 to 5 Evergreen ideas from the backlog |
| Sunday | Claude + you | Review last week's numbers and adjust scoring weights and hook styles |

**Feedback loop:** for every post, log 3-second hold rate, average watch %, shares and saves (shares and saves predict reach better than likes). Claude can compare which angles, formats and hooks won, then re-weight the rubric.

**What Claude can't do here:** read your LinkedIn feed automatically, or post to TikTok/YouTube/Instagram for you. Scheduling posts is best done in the platforms themselves or a tool like Buffer or Metricool.

## First week

- [ ] Build 2 to 3 X Lists and follow 30 to 50 AI/tech voices on LinkedIn
- [x] Create the Trend Inbox database and a Drop page in Notion
- [ ] Decide your niche angle in one line (e.g. "AI tools for non-technical people") so audience-fit scoring has a target
- [ ] Run the pipeline manually for 3 days with Claude, tweak the rubric
- [x] Set up the source pull (on demand; the daily schedule was tried and removed)
- [ ] Film the first 5 videos and start logging results
