# Technical Leadership Roadmap — Core Framework

> **Purpose:** A 5-year, domain-agnostic learning path from Senior Data Scientist toward architect-level technical leadership (technical strategy for a domain, hands-on, influence without pure management).
>
> **How to use with Claude Code:** Open this file in your repo and ask Claude Code to expand each pillar into its own note (`pillar-1-systems.md`, etc.) with concrete resources, project specs, and quarterly checkpoints. Re-run a review prompt every quarter to re-prioritize.
>
> **Time model:** Flexible. Each pillar has a *maintenance dose* (~1–2 h/week) and a *sprint dose* (~5–8 h/week). Only ever sprint on one pillar at a time.

---

## Operating Principles

1. **Build > consume.** Every book/course must terminate in an artifact: a design doc, a working system, a written decision record.
2. **Leverage existing edge.** DS rigor + MLOps + LLM/RAG experience is the differentiator — deepen the intersection, don't restart.
3. **Visibility compounds.** Half the architect role is being *known* for good judgment. Write and present what you learn.
4. **The AI engineer role (if landed) is Pillar 5 on the job** — reallocate personal time to Pillars 1 and 3.
5. **One execution plan at a time.** The [12-month Agentic AI plan](https://ai.staycurious.me) is the **Year-1 execution vehicle for Pillars 2 & 5** — this roadmap doesn't compete with it, it wraps it with the architecture (P1), strategy (P3), and visibility (P6) layers that turn an AI engineer into an architect. Don't double-schedule the same hours.
6. **Extract the pattern from the product.** The agentic plan is AWS/AgentCore-native — fine as a depth bet, but the Belgian enterprise and freelance market skews Azure/Microsoft. For every AgentCore-specific feature used (Managed Harness, Batch Evaluations, Identity), write one paragraph on the vendor-neutral pattern behind it and how you'd replicate it elsewhere (Langfuse, LiteLLM, plain OTel). That paragraph is the architect skill; the deployment is just the exercise.

---

## Pillar 1 — Systems Thinking & Architecture

*The core identity shift: from "builds models" to "designs systems and makes trade-offs explicit."*

**Skills:** distributed systems fundamentals, architecture patterns (event-driven, microservices vs. modular monolith), API/contract design, trade-off analysis, architecture decision records (ADRs), diagramming (C4 model).

**Anchor resources:**
- *Designing Data-Intensive Applications* — Kleppmann (the canonical text; read slowly, one chapter → one note)
- *Fundamentals of Software Architecture* — Richards & Ford
- *The Software Architect Elevator* — Hohpe (architect ↔ strategy bridging)
- ByteByteGo / system design primers for pattern drilling

**Artifacts:** write ADRs for real decisions at work; produce a C4 diagram + design doc for one existing system you own; redesign your homelab (jarvis) as if it were a production platform, documented.

**Milestone (Y1–Y2):** you can run an architecture review meeting and defend trade-offs in writing.

---

## Pillar 2 — Production ML & AI Platform Depth

*From "can deploy a model" to "can design the platform others deploy on."*

**Skills:** ML system design, **system design for LLM-heavy systems** (context management, retrieval architecture, caching, fallback chains, multi-model routing), feature/training-serving skew (you've already done this — write it up), model serving & scaling, **evals as an engineering discipline** (offline evals, LLM-as-judge, regression suites, eval-driven development), **observability for AI systems** (tracing, token/cost telemetry, drift & quality monitoring, tools like Langfuse/OpenTelemetry GenAI conventions), **harness engineering** (the scaffolding around models: tool interfaces, context assembly, retries, guardrails, sandboxing — increasingly where the real engineering lives), **agent security** (the lethal trifecta, OWASP Agentic Top 10, prompt-injection red-teaming — already sequenced in the 12-month plan; treat it as core, security questions are standard in senior interviews), **protocol-layer fluency** (MCP / A2A / AG-UI — learn the *architectural question* each layer answers; the version specifics churn, the questions don't), cost/latency engineering, agentic system architecture.

**Keep the DS edge alive (differentiator, not nostalgia):** the 12-month plan drops classical ML almost entirely until the capstone. Don't. Once per quarter, apply one piece of your DS rigor to an agentic system: uncertainty/calibration on agent outputs, SHAP-style attribution for tool-choice decisions, statistically sound A/B evaluation of agent variants, drift detection on production traces. The intersection of validator-grade ML rigor and agent engineering is the rarest profile in the market — and each of these is a blog post.

**Anchor resources:**
- *Designing Machine Learning Systems* + *AI Engineering* — Chip Huyen
- *Machine Learning System Design Interview* — Aminian & Xu (for pattern fluency)
- Papers/blogs: Eugene Yan, Hamel Husain, Anthropic/OpenAI engineering posts

**Artifacts:** an end-to-end reference architecture doc for an LLM/RAG platform (retrieval, evals, guardrails, monitoring); one open or internal eval harness with regression tests wired into CI; a full observability setup for one AI system (traces, cost, quality metrics on a dashboard); a written cost model for an AI workload.

**Milestone (Y1–Y3):** you're the person consulted when anyone designs an ML/AI system, not just when they build one.

---

## Pillar 3 — Business & Technical Strategy

*What separates architect from senior engineer: connecting systems to money and direction.*

**Skills:** translating business goals → technical roadmaps, build-vs-buy analysis, TCO reasoning, risk framing (you have a regulated-domain head start — generalize it), writing strategy memos, stakeholder mapping, **AI governance & the EU AI Act as a strategic asset**: you already know how to make models validator-defensible in a bank — map that experience onto AI Act obligations (risk classification, GPAI provisions, logging/traceability, human oversight requirements) for agentic systems. Nobody in the agentic engineering scene has this; every EU enterprise deploying agents needs it. It converts your "regulatory burden" frustration into your most billable consulting angle.

**Governance artifact:** one written piece per year at the intersection — e.g. "What model risk management taught me about deploying AI agents under the AI Act" or an agent-system compliance checklist mapping OWASP ASI items to AI Act articles. This is simultaneously a Pillar 3 strategy artifact and a Pillar 6 visibility magnet.

**Anchor resources:**
- *Good Strategy / Bad Strategy* — Rumelt
- *The Staff Engineer's Path* — Reilly (the single best map of this whole career direction)
- *Staff Engineer* — Larson
- *Escaping the Build Trap* — Perri (product thinking)

**Artifacts:** one 2-page technical strategy memo per quarter on a real topic at work (even unsolicited); a build-vs-buy analysis for a tool your team uses.

**Milestone (Y2–Y4):** your memos change decisions. You're invited into planning before work starts, not after.

---

## Pillar 4 — Influence, Communication & Technical Mentoring

*You already have the raw people skills — professionalize them without becoming a manager.*

**Skills:** mentoring through design review (not 1:1 management), technical writing, presenting to non-technical leadership, facilitation of architecture/RFC processes, saying no with alternatives.

**Anchor resources:**
- *The Staff Engineer's Path* (again — chapters on influence)
- *Crucial Conversations* — Patterson et al.
- Internal practice: propose/run an RFC or design-review process on your team
- External: one talk or blog post per year (meetups, internal brown-bags count)

**Artifacts:** a mentoring framework doc (what you do with your 3 mentees, systematized); one public or company-wide talk per year.

**Milestone (ongoing):** mentees and peers cite your reviews/docs as how they learned to design.

---

## Pillar 5 — Hands-On AI Engineering Credibility

*Execution vehicle: the [12-month Agentic AI plan](https://ai.staycurious.me) (MCP → A2A → AG-UI phases, AgentCore deployment, Autonomous DS Pipeline capstone). It already covers agentic development, harness engineering, evals-in-CI, security red-teaming, and cost control — follow it as written, at its ★ Core dose when time is tight.*

**This roadmap adds a thin wrapper per project (≈1 hr each):**
1. **One ADR** — the architectural decision and its trade-offs, vendor-neutral (Pillar 1 muscle).
2. **One blog post** — the comparison table, the red-team before/after, the cost model, the eval log (Pillar 6 fuel). The 12-month plan produces portfolio artifacts but never distributes them; this closes the loop.
3. **One portability note** — how the AgentCore-specific piece maps to Azure AI Foundry / self-hosted equivalents (see Operating Principle 6).

**Watch-outs on the plan itself:** protocol specifics churn fast (MCP's stateless revision, A2UI vs AG-UI) — anchor on each phase's *architectural question*, re-verify version details before each build phase rather than trusting the plan's snapshot. And its Phase-3 exit criterion "start applying for AI Engineer roles now" is correct — interview prep doubles as study.

**Milestone (ongoing):** you can prototype any new AI pattern within a weekend; every shipped project exists in three forms — running code, an ADR, and a published post.

---

## Pillar 6 — Online Visibility & Public Work

*Reputation is the asset that makes the architect title, the freelance rates, and the inbound opportunities possible. Treat it as an engineering project: consistent output > viral output.*

**Skills:** technical writing for an external audience, distilling work into shareable insights (without leaking employer specifics), building in public, basic personal-site/SEO hygiene, LinkedIn as a distribution channel (dominant in the Belgian/EU market).

**Channel strategy (pick a spine, syndicate outward):**
- **Spine: a personal blog** you own (static site in this repo → Cloudflare Pages, reusing your Civics deployment experience). Every substantial artifact from Pillars 1–5 becomes a post: ADR write-ups, eval harness lessons, harness-engineering deep dives, cost models.
- **Distribution: LinkedIn** — short posts summarizing each article; this is where Belgian recruiters, clients, and peers actually are.
- **Credibility amplifiers:** one conference/meetup talk per year (dataroots, Brussels/Leuven AI meetups, PyData); occasional open-source contributions tied to your posts (an eval tool, an MCP server).

**Cadence (flexible):** maintenance = 1 post/month + weekly LinkedIn note; sprint = weekly posts during a topic deep-dive. Batch-write with Claude Code from your Obsidian notes to fit the time budget.

**Artifacts:** live blog by end of Q1; 10 published posts in year one; a "hire me / about" page positioning you at the DS × AI-engineering × architecture intersection (dormant until freelance becomes live).

**Milestone (Y2–Y3):** inbound contact — recruiters, speaking invites, or client interest — arrives because of your writing, not your applications.

---

## Five-Year Shape (adjust freely)

| Phase | Focus | Identity checkpoint |
|---|---|---|
| **Y1** | Execute the 12-month agentic plan (= Pillar 2+5 sprint) with the ADR + blog wrapper; Pillar 1 foundations via *Staff Engineer's Path* + DDIA slow-burn; launch blog; land or shadow the AI engineer role | "Strong senior who ships agent systems and writes about them publicly" |
| **Y2** | Pillar 1 sprint + Pillar 3 start; own an architecture end-to-end; first external talk | "De facto tech lead of a system" |
| **Y3** | Pillar 3 sprint; strategy memos, cross-team influence; consider title change (staff/architect) internally or externally | "Technical leader of a domain" |
| **Y4** | Consolidate; Pillar 6 sprint (talks, series of deep-dive posts); optional: freelance groundwork leveraging architect positioning + audience | "Known expert, portable reputation" |
| **Y5** | Architect-level role secured (employed or independent); mentor pipeline running | "Technical strategy for a domain" |

---

## Quarterly Review Prompt (for Claude Code)

Every quarter, run something like:

> "Review technical-leadership-roadmap.md and my progress notes. Given [hours available], [what changed at work], and [what's shifted in the AI market], re-prioritize next quarter: which pillar to sprint, which artifact to produce, and one thing to drop."

---

## Immediate Next Actions (first 30 days)

- [ ] Split this file into per-pillar notes with Claude Code; add personal context to each
- [ ] Resume/continue the 12-month plan's Phase 1 — but retrofit the wrapper: write the ADR + portability note for whatever you've already built, and turn Project 1A/1B's framework comparison into blog post #1
- [ ] Order/queue: *The Staff Engineer's Path* (read first), *Designing Data-Intensive Applications* (slow burn)
- [ ] Write one ADR or design doc for something you're already building at work
- [ ] Apply for the AI engineer role; treat the interview prep itself as Pillar 2 study
- [ ] Blog infrastructure: you already have staycurious.me + the GitHub Pages/Cloudflare setup from ai.staycurious.me — reuse it, don't build new. Decide whether posts live on the main domain or a subdomain, publish post #1
- [ ] Draft the outline of your first governance piece (model risk management × AI agents × EU AI Act) — even 10 bullet points; it will sharpen what you notice while building
