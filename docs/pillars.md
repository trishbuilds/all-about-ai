# Content pillars

Added 2026-10-23; Working with AI widened 2026-10-24. The channel covers three things, and each needs different sources: what's happening in AI (fast news), how AI development works (explainers), and how to work well with AI and agents (practical how-tos). Tag every story with its Pillar in Trend Inbox so the mix stays balanced.

| Pillar | What a good story looks like | Best sources | Shelf life |
| --- | --- | --- | --- |
| **Trend** | A launch, a viral demo, a controversy, a big company move | X via Grok, LinkedIn News, Product Hunt, HN front page, newsletters like The Rundown AI and TLDR AI | 24 to 48h (News) |
| **How AI works** | A new research result, a model release explained, why something works or fails (agents, reasoning, context windows, benchmarks) | AI lab blogs (OpenAI, Anthropic, Google DeepMind, Meta AI), Hugging Face Daily Papers and trending models, Simon Willison's blog, Import AI, Interconnects, Andrej Karpathy, the LMArena leaderboard | Weeks (Evergreen) |
| **Working with AI** | How people actually work with AI and agents: their methodology, skills, mindset, workflows, setups and experiments (what worked, what failed, lessons learned). Your own experiments count too. Prefer first-hand accounts over generic tips. | Practitioners on X, LinkedIn, YouTube, podcasts, Substack/blogs and Reddit (e.g. Ethan Mollick, Simon Willison, Every, builders sharing setups); tool release notes (Claude Code, Cursor, ChatGPT); **your own experiments** (the Lab log) | Weeks to months (Evergreen) |

**Run one Grok prompt per pillar** instead of one general prompt, so trend news doesn't crowd out the rest. Prompts: [prompts/grok-x-search.md](../prompts/grok-x-search.md). Grok only searches X, so Working with AI finds from YouTube, podcasts, blogs and Reddit go into Drop by hand.

**Keep a lab log.** Your own experiments are the strongest source for the third pillar and the best "I tested it" material. Jot down every time an AI tool or agent surprised you, failed, or saved you time in the Notion [Lab log](https://app.notion.com/p/4022f114d1958186a49ee026e4d1faed). Treat each note as a story in Trend Inbox.

**Scoring tweaks by pillar.** For How AI works and Working with AI, velocity matters less and evergreen value matters more. Score Velocity as "is this getting attention this month" rather than "in the last 48 hours", and keep unshortlisted stories as New for up to 14 days instead of 3. For Working with AI, score Your angle high only if you can try it yourself before filming (your own Lab log experiments score 5), and kill generic, recycled tips with nothing first-hand behind them. Full rules: [config/scoring.yaml](../config/scoring.yaml).

**Weekly mix to aim for:** about 3 Trend, 2 How AI works and 2 Working with AI videos. Trend brings new viewers, and the other two build trust and followers. Each "score today" run flags any pillar running thin.
