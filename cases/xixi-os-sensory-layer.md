# OpenCLI + X Bookmarks as Personal Signal Radar

## What I Wanted to Do

I wanted a way to catch high-value AI/agent/indie-hacker signals from X without following thousands of accounts or spending hours scrolling. My bookmarks on X already contain signals I've personally verified as useful — so I used them as a first-filter layer instead of trying to monitor everything.

## Commands Used

```bash
opencli twitter timeline --limit 20 --format json
opencli twitter bookmarks --limit 10 --format json
```

## How It Works

1. Pull my own timeline and bookmarks via OpenCLI — already curated through my social graph
2. Lightweight scoring: content length + engagement to separate signal from noise
3. Human review before acting on anything

This gives me a daily digest of 20-30 signals from content I actually care about, rather than monitoring the entire X firehose.

## Why It's Better Than Monitoring Thousands of Accounts

Following 2000+ accounts means drowning in content. Using timeline + bookmarks as the first filter means content is already pre-curated — posts that passed my personal taste, got saved, or came from people I chose to follow.

Simple scoring (content length + engagement) does the second pass. High signal-to-noise ratio.

## Result

Daily digest: 20-30 items → ~25 high-value → ready for review
