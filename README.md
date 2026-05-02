## Hi, I'm Jake

I build and deploy autonomous agents: production deployments and open-source tooling for making them work better.

**Day job:** Data Engineer at PwC, Customs & International Trade. Won North America in PwC's Transfer Pricing AI competition by building and deploying an AI agent for transfer pricing risk in customs data.

**Off hours:** running a personal AI infrastructure across four networked machines and shipping vibe-coded tools.

---

### What I'm building

- **Rock** *(private)*: 24/7 multi-channel autonomous agent platform on a dedicated Mac Mini M4. Eleven Discord-fronted Claude Code sessions handle networking, content, builder/MVP work, two trading desks (swing trading and prediction markets), travel, ops, teacher mode, wiki upkeep, and an Agnes supervisor channel. Each session has its own persona, MCP servers, and skill set; memory and skills sync across networked machines via Syncthing. The whole thing runs unattended for weeks at a time.
- **Agnes** *(private)*: production AI Executive Assistant deployed for an executive at Agman Partners. She owns her own mailbox, reads inbox, drafts replies, and routes external comms back to the executive for approval before sending. Built on a custom agent runtime with SQLite persistent memory, deterministic rules-based escalation ("when unsure, escalate, don't guess"), and an extensive harness of fixture-based tests and live integration scenarios.
- **[kalshi-btc15m](https://github.com/jtsilverman/kalshi-btc15m)** *(private)*: Kalshi prediction-markets trading agent live on dedicated VPS, betting on 15-minute Bitcoin price direction. Stacking ensemble of LightGBM, CatBoost, and TabPFN with Venn-ABERS calibration to turn raw model outputs into honest probabilities, Kelly criterion position sizing, and combinatorial purged cross-validation to keep training and validation periods cleanly separated (the standard escape route for time-series leakage).
- **[travel-concierge](https://github.com/jtsilverman/travel-concierge)**: self-hostable AI travel planner. Chat with Claude to search real flights, hotels, and restaurants, then build a visual day-by-day itinerary with maps and a budget breakdown. Single-binary deploy you can run on your own machine without sending your travel data through someone else's hosted service.
- **[gridplay](https://github.com/jtsilverman/gridplay)**: browser-based playground for ARC-AGI-3, the Abstraction and Reasoning Corpus benchmark designed to measure abstract pattern recognition that current LLMs are bad at. Pit Claude, GPT-4o, and Gemini against the same puzzles and watch them reason their way through (or not).
- **[tracediff](https://github.com/jtsilverman/tracediff)**: pytest-style snapshot testing for AI agents. Capture agent behavior on a fixed input set, diff future runs against the snapshot, surface silent regressions before they hit production. Designed to wire into CI alongside your existing test suite.
- **[proxyprof](https://github.com/jtsilverman/proxyprof)**: transparent STDIO proxy that profiles MCP agent sessions without modifying the agent. Drop-in middleware between Claude (or any MCP client) and an MCP server; emits per-tool latency, error rates, message counts, and a session timeline you can replay.
- **[policygrade](https://github.com/jtsilverman/policygrade)**: quality scorer for Claude Code skills, grading against Anthropic's official best-practices checklist (frontmatter completeness, trigger specificity, instruction clarity, and so on). CLI for local checks plus a public web directory ranking shared community skills.
- **[council](https://github.com/jtsilverman/council)**: multi-perspective LLM deliberation CLI, inspired by Karpathy's llm-council. Spin up several expert personas (security reviewer, performance reviewer, naming reviewer, etc.), have each one weigh in on a question or diff, then synthesize the disagreement into a final recommendation.
- **[probe](https://github.com/jtsilverman/probe)**: zero-config AI code review CLI. Catches the AI-generated code anti-patterns conventional linters miss: redundant defensive checks, abandoned partial implementations, fake-test ratification of buggy code, fabricated APIs.
- **[browser-bench](https://github.com/jtsilverman/browser-bench)**: Advent-of-Code-style browser automation challenges for agents. Eight escalating tasks (login flow, dynamic content, multi-tab coordination, form filling, etc.) shipped as a single Go binary with built-in verification, so any browser-control agent can be benchmarked in minutes.
- **[ctxpeek](https://github.com/jtsilverman/ctxpeek)**: VS Code extension that surfaces what context GitHub Copilot has access to. Shows the file list, flags sensitive files (.env, credentials, anything matching .copilotignore patterns), and emits a real-time exposure dashboard so you can audit what's been silently fed to the model.

---

**Stack:** Python, Go, Rust, TypeScript, Claude Code, MCP, Anthropic SDK

**Methodology:** Spec-driven development, failing-test-first, multi-model cross-source verification

**Reach me:** jtsilverman8@gmail.com · [LinkedIn](https://linkedin.com/in/jacob-silverman1/)
