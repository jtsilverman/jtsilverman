# Jake Silverman

Build autonomous AI agents, the data infrastructure under them, and the open-source tooling around them.

Data Engineer at PwC, Customs & International Trade. North America winner, PwC Transfer Pricing AI competition.

---

## Production deployments

### Rock *(private)*
24/7 multi-channel agent platform on a dedicated Mac Mini M4. Eleven Discord-fronted Claude Code sessions cover networking, content, builder/MVP work, two trading desks, travel, ops, teacher mode, wiki upkeep, and an Agnes supervisor channel. Each session has its own persona, MCP servers, and skill library; memory and skills sync across four networked machines (Mac Mini, Mac Studio, laptop, Hetzner VPS) via Syncthing. Runs unattended for weeks at a time.
**Stack:** Claude Code, MCP servers, launchd, Tailscale, Syncthing, fswatch, Discord API.

### Agnes *(private)*
Production AI Executive Assistant deployed for an executive at Agman Partners. Owns her own mailbox, reads inbox, drafts replies, and routes external comms back to the executive for approval before sending. Custom agent runtime with SQLite persistent memory and rules-based escalation ("when unsure, escalate, don't guess"); fixture-based test harness plus live integration scenarios.
**Stack:** Node.js, OpenClaw runtime, Microsoft Graph API, SQLite.

### [kalshi-btc15m](https://github.com/jtsilverman/kalshi-btc15m) *(private)*
Live Bitcoin-direction trading agent on Kalshi prediction markets, running 24/7 on dedicated VPS. Stacking ensemble of LightGBM, CatBoost, and TabPFN with Venn-ABERS calibration for honest probabilities, Kelly-criterion position sizing, and combinatorial purged cross-validation to prevent temporal data leakage.
**Stack:** Python, scikit-learn, LightGBM, CatBoost, TabPFN, Pandas, Kalshi API.

---

## Open-source agents

### [travel-concierge](https://github.com/jtsilverman/travel-concierge)
Self-hostable AI travel planner. Chat with Claude to search real flights, hotels, and restaurants, then build a visual day-by-day itinerary with maps and a budget breakdown. Designed as a single-binary deploy so you can run it on your own machine without sending travel data through someone else's hosted service.
**Stack:** Python, Anthropic SDK, SerpAPI, Google Places API, SQLite.

### [gridplay](https://github.com/jtsilverman/gridplay)
First browser-based playground for ARC-AGI-3, the abstract reasoning benchmark designed to measure pattern recognition that current LLMs are bad at. Pit Claude, GPT-4o, and Gemini against the same puzzles; React frontend renders frames on HTML Canvas with pixelated upscaling, reasoning log on the side.
**Stack:** Python backend, React frontend, Canvas API, Anthropic / OpenAI / Gemini APIs.

---

## Agent development tooling

### [tracediff](https://github.com/jtsilverman/tracediff)
Pytest-style snapshot testing for AI agents. Capture agent behavior on a fixed input set, diff future runs against the snapshot, surface silent regressions before they ship. Designed to wire into CI alongside an existing test suite.
**Stack:** Go.

### [proxyprof](https://github.com/jtsilverman/proxyprof)
Transparent STDIO proxy that profiles MCP agent sessions without modifying the agent. Drop-in middleware between Claude (or any MCP client) and an MCP server; emits per-tool latency, error rates, message counts, and a replayable session timeline.
**Stack:** TypeScript, MCP protocol.

### [policygrade](https://github.com/jtsilverman/policygrade)
Quality grader for Claude Code skills, scored against Anthropic's official best-practice rubric (frontmatter completeness, trigger specificity, instruction clarity, etc.). CLI for local checks plus a public web leaderboard ranking community skills, refreshed daily via GitHub Actions.
**Stack:** Go, GitHub API, GitHub Actions.

### [probe](https://github.com/jtsilverman/probe)
Zero-config AI code review CLI. Catches AI-generated anti-patterns conventional linters miss: redundant defensive code, abandoned partial implementations, fake-test ratification of buggy code, fabricated APIs.
**Stack:** Go, Anthropic SDK.

---

## Multi-model evaluation

### [council](https://github.com/jtsilverman/council)
Multi-perspective LLM deliberation CLI, inspired by Karpathy's llm-council. Spin up several expert personas (security reviewer, performance reviewer, naming reviewer, etc.), have each weigh in on a question or diff, then synthesize the disagreement into a final recommendation. Default mode uses `claude --print` (no API key needed).
**Stack:** Go, Anthropic / OpenAI / Gemini / OpenRouter APIs.

### [browser-bench](https://github.com/jtsilverman/browser-bench)
Advent-of-Code-style browser automation challenges for agents. Eight escalating tasks (login flow, dynamic content, multi-tab coordination, form filling, etc.) shipped as a single Go binary with built-in verification; benchmarks any browser-control agent in minutes.
**Stack:** Go.

---

## Editor / context

### [ctxpeek](https://github.com/jtsilverman/ctxpeek)
VS Code extension that surfaces what context GitHub Copilot has access to. Shows the file list, flags sensitive files (.env, credentials, anything matching .copilotignore patterns), and emits a real-time exposure dashboard so you can audit what's been silently fed to the model.
**Stack:** TypeScript, VS Code Extension API, Webview.

---

## Contact

jtsilverman8@gmail.com · [LinkedIn](https://www.linkedin.com/in/jacob-silverman1/)
