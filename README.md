<div align="center">

# Akshay Bengani

**I build agent systems for work, and small finished software for problems I actually have.**

MCP servers and evaluation harnesses by day. Offline apps, mostly for one person I know by name, by night.

[![Website](https://img.shields.io/badge/akshaybengani.com-0D47A1?style=flat-square)](https://akshaybengani.com/)
[![X](https://img.shields.io/badge/@benganiakshay-0D47A1?style=flat-square)](https://x.com/benganiakshay)
[![Email](https://img.shields.io/badge/akshaybengani@gmail.com-0D47A1?style=flat-square)](mailto:akshaybengani@gmail.com)

</div>

---

## The day job: agent systems

I work in implementation and technical enablement on an enterprise agent platform, which in
practice means building the thing and then proving it works.

**MCP servers in production.** Built and deployed servers that back a live alerting system,
from scoping through deployment, QA, and handover. Along the way I found two protocol defects
that had left both servers unusable by any compliant client, because the tests mocked the
transport instead of speaking it.

**Evaluation, not assertion.** A probe runner and two 43 case batteries, measuring detection
rates across configurations. An agent that sounds right and an agent that is right are
different claims, and only one of them survives a battery.

**The unglamorous half.** Production escalations root caused and shipped, runbooks, QA reports,
and the occasional load bearing claim withdrawn once I'd found I couldn't support it.

## The night job: things I finished

Each one started because something in my own life didn't have a tool, and every app I found
solved a neighbouring problem instead of the real one.

| Project | What it is | Built with |
| :--- | :--- | :--- |
| **[Hisaab](https://github.com/akshaybengani/Hisaab)** | A fully offline ledger for handing out things at cost and collecting the cash back. It isn't inventory, it tracks who owes you money and treats stock as a by-product. | Flutter · 416 tests |
| **[Medstock](https://github.com/akshaybengani/Medstock)** | An offline stock book for a household's medicines. Not a pill reminder, a logistics ledger: what's left, when it runs out, and what to order to reach a given date. | Flutter |
| **[MyPlaces](https://github.com/akshaybengani/MyPlaces)** | An offline field notebook for houses you visit on foot, for the half of the world whose address is a lane, a landmark, and a family name. | Flutter |
| **[Token Counter](https://github.com/akshaybengani/token-counter)** | Today's token spend across Claude Code, Codex, Gemini CLI, and Cursor, as a ring against a daily target you set. Reads files those tools already wrote to disk. | Swift · macOS |
| **[GitGlance](https://github.com/akshaybengani/gitglance)** | A menu bar dashboard for every git repo on your Mac. Not a git client, a guardrail: which repos have work sitting on a branch it should never have landed on. | Swift · macOS |
| **[Replay](https://github.com/akshaybengani/ReplayAutomation)** | A macOS menu bar macro recorder. Do a task by hand once, and it does it again while you go elsewhere. | Swift · 116 tests |
| **[Barge](https://github.com/akshaybengani/barge)** | A queue for file operations. Not a faster copier, a scheduler for copies that verifies what arrived matches what left before deleting an original. | Electron · TypeScript |

Two more are still private while they settle: **SoundA2Z**, a Rust control plane for per-app
volume and synchronized multi-room audio zones that an assistant can drive over MCP, and
**MYOCA**, a bring-your-own-key Android chat agent with no backend and no login, where each
agent is granted device capabilities one at a time.

## The thread running through them

I keep arriving at the same four decisions, so they're worth stating once.

**No network unless the problem needs one.** Most of these make zero network calls. That isn't
a feature I added, it's a constraint I started from, and it removes accounts, sync conflicts,
outages, and the entire question of what happens to somebody's data.

**Derive state, never decrement it.** Medstock computes what's left from a snapshot plus what's
happened since, rather than mutating a running total. A counter that drifts is impossible to
audit. A derivation you can recompute is impossible to lose.

**The README is part of the build.** Every project opens with the problem in plain language
before it mentions a single feature, because a stranger gives you about one screen before
deciding.

**Tests are the finish line, not the intention.** Counts on the badges are real and they run.

## What I work in

**AI and agents** · MCP server development, agent evaluation and probe batteries, RAG with LangChain and FAISS, LangGraph, Google ADK, multi-agent orchestration. I work with Claude Code daily and build the tooling around it.

**Mobile** · Flutter and Dart since 2019. Offline-first architecture, local persistence, on-device media, Play Store releases. Before that, a PCI-DSS compliant fintech platform for under-18s.

**Desktop** · Swift and SwiftUI for macOS (menu bar apps, accessibility APIs, event tap recording, zero dependencies). Rust where it has to be fast, Electron where it has to run on Windows too.

**Before all of that** · Java and Android, Swift and UIKit, Node, React, Go, and a long stretch of Python automation. Most of it is still public in this account, which is why you'll find about a hundred repos behind the seven above.

<div align="center">

Ideas, or a project you think I'd enjoy? **[akshaybengani@gmail.com](mailto:akshaybengani@gmail.com)**

</div>
