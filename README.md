# Null-Phnix

I build autonomous AI agents and local LLM infrastructure. Everything runs on my hardware. Nothing leaks to the cloud unless I choose it.

---

## What I work on

- **Autonomous agents** — systems that run overnight, unsupervised, and actually finish the job
- **Local LLM infrastructure** — RAG pipelines, fine-tuning, model distillation on consumer hardware
- **MCP servers** — tools that let Claude Code control real systems as tool calls
- **Browser automation** — stealth-first scraping and research agents that survive on real websites
- **Audio intelligence** — AI that genuinely listens to and understands music
- **Terminal tools** — TUI dashboards, voice synthesis, GitHub workflows, all in the shell

---

## Current projects

| Project | What it does | Stack |
|---------|-------------|-------|
| [Huginn](https://github.com/Null-Phnix/Huginn) | Self-hosted Firecrawl alternative. Scrape, crawl, map, extract, research, watch — with NDJSON streaming, graph mapping, change detection, and vector memory | Python, Playwright, FastAPI, ChromaDB |
| [Blackreach](https://github.com/Null-Phnix/Blackreach) | Autonomous browser research agent. ReAct loop, DOM walker with numeric IDs, stealth Playwright, cross-session SQLite memory, 2,904 tests | Python, Playwright, Rich, Click |
| [Claud-Ear](https://github.com/Null-Phnix/claud-ear) | Give your AI agent the ability to listen to and understand music — deep analysis, stem separation, lyrics transcription, beat generation | Python, torch, librosa, Whisper, Demucs |
| [Claude Voice](https://github.com/Null-Phnix/claude-voice) | The missing half of Claude Code's voice mode. TTS with karaoke-style word highlighting. Fully local, zero API keys | Python, Kokoro, sounddevice |
| [JobHound](https://github.com/Null-Phnix/jobhound) | MCP server that scans, scores, and applies to jobs via Ashby, Greenhouse, and Lever APIs. TUI dashboard included | Python, fastmcp, httpx, Textual |
| [Apple Calendar MCP](https://github.com/Null-Phnix/apple-calendar-mcp) | MCP server for Apple Calendar integration with natural language scheduling | TypeScript, Node.js, AppleScript |
| [ghboard](https://github.com/Null-Phnix/ghboard) | GitHub terminal dashboard — contribution heatmap, starred repo manager, notification center | Go, Bubble Tea, GitHub GraphQL |

### Stats

- **Huginn**: v1.2.0 · 343 tests · 1,671 pages/sec crawl throughput · MIT
- **Blackreach**: v5.0.0-beta.2 · 2,904 tests · multi-provider LLM · MIT
- **Claud-Ear**: v1.0.0 · MCP server · 8 audio tools · MIT

---

Python · Go · TypeScript · Claude API · Playwright · FastMCP · Textual · ChromaDB · LlamaIndex · SQLite · Kokoro · librosa · PyTorch

### Reach me

[phnix.dev](https://phnix.dev) · [contact@phnix.dev](mailto:contact@phnix.dev)
