# What you've done since April 2026

Reconstructed from 174 GitHub repos, 24 local git repos, your Mindset timesheet
(20 Jul to 14 Sep), 22 TE Manager engagements, and 29 Memex specs.

The headline: **the April resume describes a job you no longer have.** It says
"Full Stack Sr. Developer, Jun 2025 to Present, internal innovation and upskilling
at PSI". Since 20 July you've been doing Implementation and Technical Enablement
at Mindset AI, which is a different job with different evidence behind it.

---

## The shape of the period

| Window | What you were doing |
| :--- | :--- |
| Apr to early Jul 2026 | PSI internal engineering: AI SDLC tooling, CI/CD autofix, React apps |
| 20 Jul 2026 to now | Mindset AI, Implementation and Technical Enablement |
| Throughout, evenings | A personal shipping streak: 11 apps, 4 languages |

---

## Part 1: PSI work, April to early July

**Aegis AI** (`akshaybengani-psi/aegis-ai`, 12 commits, Apr to May)
A containerized agent that runs on a GitLab CI/CD schedule, scans the issue tracker
for `Autofix` or `Analyze` labels, dispatches AI agents to fix them, and reports back
as comments and merge requests. You added Claude and Anthropic provider support,
OpenHands integration, Docker packaging, and the logging layer. Reached v3.3.9.
This is the strongest PSI artifact and the resume doesn't mention it.

**Playbook and playbook-plugin** (`psi-portal/*`, 78 commits, Apr to May)
An AI SDLC system for scaling dev teams: a Claude Code plugin for the PSI Portal
(.NET 8, EF Core, PostgreSQL, React 18, Vite, MUI, Azure AD/MSAL) with slash commands,
six specialised subagents, hooks, and rules, plus a companion knowledge repo of skills,
epics, and feature docs. You deepened the planner, code-reviewer, and tdd-guide agents,
and scaffolded a 14-ticket workshop extraction from the invoicing epic.

**AI Fortnight 2026 workshops** (`ai-fortnight-2026/ws01` to `ws05`, Apr)
Five agentic-AI teaching workshops: first contact, stateful journeys, knowledge at
scale (RAG with LangChain, FAISS, configurable Gemini or Hugging Face embeddings),
self-healing agents, and the agent squad. You authored the RAG and guardrails
implementations and the provider-configuration flow.

**PSI Resume Builder** (`resume-builder/frontend`, 50 commits, Apr to Jun)
React frontend. You added Claude OAuth token login support and the logging layer.

**Also:** `psi_c2o_app` (Flutter, to early Jul), `psi-narayana` microservices,
and an Azure DevOps deployment demo.

---

## Part 2: Mindset AI, 20 July to present

Role in the timesheet: **Implementation and Technical Enablement**. Six workstreams.

### LCG Safeguarding alerts (spec-26) — the flagship
Six weeks, roughly 14 Aug to 9 Sep, the single largest piece of work in the period.

You built and shipped **two MCP servers** for Learning Curve Group's safeguarding
notification system, deployed live, and took them from scoping to a delivered
customer handover. Specifically:

- Scoped spec-26 into 11 decisions and 12 tasks, then closed the decisions
- Built the notification MCP server and stood up an INT test agent
- Wrote a **probe runner and two 43-case test batteries**, and measured real
  detection rates (66% on one config, 57% on LCG's)
- Fixed two MCP protocol bugs and shipped a tool-name collision guard
- Got all **11 safeguarding plans live and firing**, verified by reading Firestore
- Proved the acceptance criterion end to end with a delivered alert email
- Found and replaced **US crisis helplines that were live in four plans** for a
  UK customer, which is a genuine safeguarding catch
- Wrote the Mindset Analytics emitter, hit an IAM block on the BigQuery route,
  and built a temporary self-hosted demo stack around it
- Raised roughly 20 tracked issues, wrote runbooks, QA reports, a governance
  statement, an assumptions register, and an explainer PDF for the customer
- Demoed to the account lead and worked through his four action points, including
  **withdrawing a load-bearing claim** you'd found you couldn't support

That last detail is worth keeping. Disproving your own hypothesis and retracting a
claim in front of a customer is a seniority signal that no skills list conveys.

### AMS production escalations (10 to 13 Aug)
Escalation #163: diagnosed, fixed, merge request raised, merged, deployed to staging,
then **to production**. Escalation #164: Firebase and Firestore diagnosis and
root-cause analysis, which became spec-207. You also wrote a platform learnings doc
and a slack-post skill.

### Meridian Contribution Concierge POC (30 Jul to 7 Aug)
An open-source contribution onboarding agent, built A to Z as a training build.
MCP spec, deployment and secrets research, anonymous access, deployed and submitted.

### M4 platform (Jul and Sep)
The agent-first platform rebuild. You cloned eight GitHub repos and wrote the
workspace routing and architecture docs, and traced and fixed the te-hub and
Mindset MCP connections.

### Testing and QA
Test Bash sessions (including the Mindset Meter MCP session on 3 Sep), probe
batteries, manual testing on INT and staging, and defect reporting.

### Enablement tooling
Authored the `te-manager` skill, onboarded to TE Manager, and shared your working
practice in `#claude-best-practice`.

**Breadth of the portfolio you've touched:** 22 customer engagements and 29 specs
across FTL, HealthStream, Coverflex, eduMe, Mintra, Hult, LCG, Meridian, Ceannas,
Odilo, Fuse, Access Infinity, and Xplor.

---

## Part 3: Outside Mindset

Eleven applications, four languages, most of them finished rather than abandoned.

### Shipped and public
| Project | What | Stack | Since |
| :--- | :--- | :--- | :--- |
| **Hisaab** | Offline ledger for goods handed out at cost | Flutter, 416 tests | 9 Sep |
| **Medstock** | Offline household medicine stock book | Flutter | 31 Aug |
| **MyPlaces** | Offline field notebook for door-to-door visits | Flutter | 28 Aug |
| **Token Counter** | Token spend across 4 AI CLIs as a desktop ring | Swift, macOS | 7 Sep |
| **GitGlance** | Menu bar guardrail across every git repo | Swift, macOS | 12 Aug |
| **Replay** | macOS macro recorder | Swift, 116 tests | 31 Aug |
| **Barge** | Verified file-transfer queue | Electron, TypeScript | 7 Sep |

### Substantial but not yet public
| Project | What | Stack | Commits |
| :--- | :--- | :--- | :--- |
| **SoundA2Z** | Per-app volume and multi-room audio zones with an MCP control plane | **Rust**, 4 repos | 143 since 9 Sep |
| **HomeBook** | Local-first household inventory with a shared identity layer | Flutter, Firebase | 168 since 1 Sep |
| **MYOCA** | BYOK Android chat agent, no backend, no login, per-agent device permissions | Flutter, private | 145 since 6 May |

### AI and LLM side work
- **Multi-Model-Chat-Playground** (Jul), **PAI-OpenAI-Wrapper** (Jul)
- **project-friday**, a self-improving voice agent built on Hermes Agent
- **custom-ai-agents**, which became MYOCA
- **akshaybengani.com**, the Astro rebuild

---

## What the April resume is missing

**The job itself.** Mindset AI, Implementation and Technical Enablement, from 20 July.
Nothing in the resume reflects it.

**MCP server development in production.** You've shipped MCP servers to live customers
and fixed protocol-level bugs in them. The resume lists "FastMCP" as a bullet in a
skills grid, which undersells it by a wide margin.

**Agent evaluation.** Probe runners, 43-case batteries, measured detection rates,
regression cases. This is the scarcest skill on the list and it appears nowhere.

**Languages you now actually ship in.** Swift and SwiftUI (three macOS apps), Rust
(SoundA2Z), Electron. The resume's skills grid has none of them.

**Production incident work.** Two AMS escalations diagnosed and taken to production.

**Volume.** Eleven apps shipped outside work in about five months, seven of them public.

---

## Two cautions

**Customer names are probably confidential.** LCG, FTL, HealthStream, Hult and the
rest appear in internal tooling. A resume can describe them as "a UK further-education
provider" and so on. Nothing customer-identifying should go near the public GitHub
profile.

**The resume's framing is stale in a second way.** It leads with "Mobile Applications
Architect | Full Stack Sr. Developer". The last five months say something more specific:
you build and evaluate agent systems, and you ship desktop and mobile tools on the side.
