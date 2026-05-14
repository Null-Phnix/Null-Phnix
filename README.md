# Null-Phnix 🜏

> *"I don't trust the cloud. I build agents that run on my hardware, overnight, unsupervised, and finish the job. If I need a service, I build it. If I need a model, I run it locally. Nothing leaks unless I choose it."*

---

## Why I Build

I'm 25, Toronto, running this whole operation off a Linux desktop (RTX 4060, 8GB VRAM) and an M4 MacBook at work. I've got two Ollama Max Pro subscriptions giving me unlimited cloud inference on both machines — and I *still* spend half my time fighting latency and OOM errors.

My whole ecosystem exists because I got tired of depending on services that either:
- Cost money I don't have
- Leak data I don't want leaked
- Break when I need them at 3am
- Don't let me run them unsupervised for 8 hours

So I built replacements. All of them.

---

## The Ecosystem

These aren't hobby projects — they're infrastructure I've built to replace SaaS I refuse to pay for or trust.

| Project | What It Replaces | Why I Built My Own |
|---------|-----------------|-------------------|
| [**Huginn**](https://github.com/Null-Phnix/Huginn) | Firecrawl / ScrapeGraph / paid scraping APIs | Per-page pricing is a scam. I crawl thousands of pages for free at 1,671 pages/sec. Graph mapping, change detection, vector memory — all local. |
| [**Blackreach**](https://github.com/Null-Phnix/Blackreach) | Browser agents that die on CAPTCHAs, agents that don't finish, agents that hallucinate DOM elements | Real research needs a ReAct loop that can survive real websites. 2,904 tests because the real web is hostile. |
| [**Deep Video Watcher**](https://github.com/Null-Phnix/deep-video-watcher) | Shallow "AI summary" tools, manual video scrubbing, overpriced editing software | I watch 45-min theory videos and forget them. This actually comprehends video content — structured understanding, edit-by-reference, beat-sync extraction. |
| [**Claud-Ear**](https://github.com/Null-Phnix/claud-ear) | Music analysis SaaS, manually listening to tracks | My agent should understand music like I do — stem separation, key detection, beat analysis, lyrics transcription, all as tool calls. |
| [**JobHound**](https://github.com/Null-Phnix/jobhound) | LinkedIn Easy Apply, manual job board browsing, paying for premium job alerts | Ashby / Greenhouse / Lever APIs are free. Why am I manually scrolling? MCP server — autonomous scanning, scoring, applying. |
| [**Apple Calendar MCP**](https://github.com/Null-Phnix/apple-calendar-mcp) | Apple's garbage Calendar.app manual scheduling | Natural language scheduling via MCP. "Lunch with Sarah at 1pm" → calendar entry. |
| [**Claude Voice**](https://github.com/Null-Phnix/claude-voice) | Cloud TTS that costs per-character, voice modes that don't exist for terminal users | Fully local TTS with karaoke-style word highlighting. Zero API keys. One file. 17 stars because people actually needed this. |
| [**ghboard**](https://github.com/Null-Phnix/ghboard) | GitHub's web UI for everything | Terminal dashboard — contribution heatmap, starred repo manager, notifications. I live in the terminal. |

---

## Current Pain Points

These are the fights I'm actively losing:

1. **8GB VRAM is not enough** — I have to unload Whisper to run Ollama, unload Ollama to run Demucs, juggle models like a clown. Every tool I build has graceful degradation because I literally cannot run everything at once.

2. **Ollama cloud latency compounds** — A single vision inference takes 4-6s locally. Fine. But comprehension pipelines need 50+ frames. That's 5 minutes of waiting for 30 seconds of "understanding."

3. **The MacBook is a backup, not a peer** — It lives at work. My Linux desktop is at home. They share a Google Drive. This is not a multi-device architecture, it's a workaround with extra steps.

4. **Every project is a monolith** — Huginn does scraping. Blackreach does browser research. Deep Video Watcher does video. They don't share state, memory, or context. I want them to be one unified agent swarm.

5. **I'm a one-man team building 8 projects** — Context switching is real. The DEV_LOGs in Blackreach are as long as the code because I forget why I chose SQLite over ChromaDB, or whether I already fixed that stealth issue.

---

## End Goals — Where This Is Headed

### Short Term (now → 3 months)
- **Stable multi-device agent coordination** — Huginn on Linux, Blackreach on Mac, one brain across both
- **Persistent knowledge graph** — everything scraped, watched, heard, and read feeds into a cumulative understanding
- **Fully local autonomous research** — "Find me every paper arguing X against Y in the last 2 years, rank by citation strength, summarize disagreements"

### Medium Term (3–6 months)
- **Agent swarm with specialized workers** — scraper, researcher, editor, music analyst, video producer, all coordinated
- **Cross-project memory** — Blackreach findings inform Huginn crawl prioritization; video comprehension feeds the knowledge base
- **Self-improving agents** — agents that generate their own test cases, find their own bugs, patch their own code

### Long Term (6–12 months)
- **Full autonomy** — "Watch these 10 videos, extract the arguments, find contradictions, write a response, edit a video reply, and post it"
- **Personal AGI stack** — not a single model, a system of models + tools + memory + reasoning that operates better than I could manually
- **Economic independence** — every tool I need already exists, on my hardware, under my control

---

## Stats

| Project | Version | Tests | Status |
|---------|---------|-------|--------|
| Huginn | v1.2.0 | 343 passing | Active |
| Blackreach | v5.0.0-beta.2 | 2,904 passing | Active |
| Deep Video Watcher | v0.2.0 | 16 modules, 16 tests | Active |
| Claud-Ear | v1.0.0 | 8 audio tools | Active |
| Claude Voice | v0.1.0 | — | Stable |
| JobHound | v0.1.0 | — | Active |
| Apple Calendar MCP | v1.0.0 | — | Stable |
| ghboard | — | — | Stable |

---

## Tech Stack

**Languages:** Python · Go · TypeScript
**Models:** Ollama (local + cloud) · Claude API (when cloud necessary) · Whisper · LLaVA · Kokoro TTS
**Infrastructure:** Playwright · FastAPI · FastMCP · ChromaDB · SQLite · FFmpeg · Demucs · Bubble Tea
**Philosophy:** Local-first. Autonomous. Graceful degradation. Test everything.

---

## What I'm Looking For

Not job offers. Not investors. Not collaborators who want to "chat" for 6 weeks.

- **People building the same thing** — if you're trying to run agent swarms locally, hit me up. I need peers, not fans.
- **Better hardware** — if you have a spare 24GB GPU you're not using, I will actually put it to work.
- **Criticism** — find data to disprove my models, find bugs in my code, find edge cases my tests miss. "Looks cool" is noise. "This breaks when X" is signal.

---

> *"The board is rigged, but natural selection operates on revealed outcomes regardless of intent. If society can't help those men, the casualties are features."*>
> — My framework for the world, applied to code

---

**phnix.dev** · [contact@phnix.dev](mailto:contact@phnix.dev)
