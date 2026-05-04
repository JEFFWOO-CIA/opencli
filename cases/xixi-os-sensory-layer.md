# OpenCLI as Sensory Layer for Personal AI OS

## What I Wanted to Do

Build a personal AI operating system (西西 OS) that continuously watches high-signal external content, filters it through my own judgment and taste, and converts signals into actionable content assets or business opportunities — all without getting drowned in noise.

The core question I needed to answer daily: **"Which external signals actually matter for my one-person company, and what can I do with them this week?"**

## Which Commands I Used

```bash
# Primary sensory layer — my personal timeline
opencli twitter timeline --limit 20 --format json

# Verified high-value content I've already bookmarked
opencli twitter bookmarks --limit 10 --format json

# Used during initial account pool validation
opencli twitter search "from:<handle>" --limit 3 --format json
opencli twitter profile <handle> --format json
```

## How It Works Together

My setup is a layered pipeline:

```
opencli twitter timeline + bookmarks
    → x_account_signals_collector.py (filters for engagement)
    → x_signals JSON (canonical storage)
    → xixi-external-mastery-loop.py (source: x_signals)
    → OpenClaw harness (brain/routing)
    → Founder Opportunity Cards (validated by taste + data)
    → Content asset or monetization experiment
```

Key insight: **I don't monitor 2000+ X accounts.** Instead, I let my own timeline and bookmarks be the first filter — content that's already been curated by my social graph and past choices. Then a lightweight scoring layer (content length + engagement) extracts what's worth processing.

The `x_signals` source in `xixi-external-mastery-loop.py` joins the same pipeline as `garry_x`, `gbrain_repo`, `nous_os` and other knowledge sources. Everything gets ranked together.

## The Result

- **Daily signal cards** from my timeline/bookmarks — 20-30 cards, filtered to ~25 high-value
- **Founder Opportunity Cards** generated from signals that pass Mason-fit, monetization path, and first-experiment criteria
- **One human gate** before anything gets published or monetized
- Built with ~200 lines of Python on top of existing opencli commands

## Why This Is Different from Typical Usage

Most people use OpenCLI as a direct tool: fetch this page, search that query.

I use it as a **sensory nervous system** — a continuous, automated input layer for an AI agent. The commands themselves are simple; what makes it powerful is the pipeline wrapping them: scheduled collection + filtering + canonical storage + multi-source ranking + human judgment gate.

OpenCLI is the eyes and ears. OpenClaw is the brain. The distinction matters when you're trying to build a system that runs while you sleep.

## Files

- Collector script: `workspace/scripts/x_account_signals_collector.py`
- Digest generator: `workspace/scripts/x_account_signals_digest.py`
- External mastery loop with x_signals source: `workspace/scripts/xixi-external-mastery-loop.py`
- Founder Opportunity Cards: `vault/research/founder-opportunities/samples/`

## Tags

`personal-os`, `twitter`, `signal-curation`, `founder-intelligence`, `openclaw-integration`
