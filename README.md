# agent-usage

Public JSON feed for Mario's Agent Usage home-screen widget.

**Feed:** `agent-usage.json` in this repo — raw URL:
https://raw.githubusercontent.com/Super-Mario-OG/agent-usage/main/agent-usage.json

One entry per agent (Muse, Claude, ChatGPT, Gemini, Grok Bot) with
percent left, percent used, plan, reset time, and a `reported_at`
timestamp. Updates are merged with a fresher-wins rule: a report only
replaces an entry when its `reported_at` is strictly newer, so stale
data can never overwrite fresh data. Muse's entry is refreshed live
every hour by a scheduled job; the other agents report twice a day.
