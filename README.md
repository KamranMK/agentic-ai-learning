# Agentic AI Engineer — Learning Plans

Personal learning roadmaps for transitioning from Data Scientist / ML Engineer to **Agentic AI Engineer**. Two versions, two different bets:

🌐 **Live at:** [ai.staycurious.me](https://ai.staycurious.me) (serves `index.html`)

## Structure
- `index.html` — **12-month, protocol-first** plan: AWS Bedrock AgentCore, MCP → A2A → AG-UI, capstone is an Autonomous DS Pipeline Agent.
- `holmes.html` — **8-week, job-targeted sprint**: multi-LLM routing (Claude/GPT/Gemini/Qwen/GLM/Kimi/Gemma), browser-agent automation (Stagehand/BrowserUse/Playwright MCP), multi-agent architecture, and evals/benchmarks — built to match a Founding AI Engineer role at an agentic-QA startup (Holmes).
- `README.md` — this file

## index.html — Phases
| Phase | Months | Protocol layer | Key build |
|-------|--------|---------------|-----------|
| 1 | 1–3 | MCP (tools) | Typed research agent: PydanticAI → Strands → MCP wiring |
| 2 | 4–6 | A2A (agents) | Cross-framework A2A handoff + incident response on AgentCore |
| 3 | 7–9 | AG-UI (users) | Streaming UI + production hardening (OTel, Guardrails, Evaluations) |
| 4 | 10–12 | Capstone | Autonomous DS Pipeline Agent spanning all 3 protocol layers |

## holmes.html — Phases
| Phase | Weeks | Focus | Key build |
|-------|-------|-------|-----------|
| 1 | 1–2 | LLM fundamentals & multi-provider mastery | Provider bake-off (cost/latency/quality) across Claude/GPT/Gemini + an open-weight model |
| 2 | 3–4 | Browser automation stack | Same UI flow in Stagehand, BrowserUse, and Playwright MCP + a resilience test |
| 3 | 5–6 | Multi-agent architecture & evals | Planner → executor → critic test generator + cross-provider eval harness |
| 4 | 7–8 | Capstone & readiness | Autonomous QA Agent (planner → browser-executor → critic → reporter) + portfolio artifacts |

## Deployment
GitHub Pages on `main` branch root, served at `ai.staycurious.me` via Cloudflare CNAME → `KamranMK.github.io`. Only `index.html` is the live homepage; `holmes.html` is reachable as a direct page but isn't linked from navigation.

*Last updated: June 2026*
