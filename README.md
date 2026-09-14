<div align="center">

# Akshay Bengani

**I build small, finished software for problems I actually have.**

Mostly offline, mostly private, usually for one person I know by name.

[![Website](https://img.shields.io/badge/akshaybengani.com-0D47A1?style=flat-square)](https://akshaybengani.com/)
[![X](https://img.shields.io/badge/@benganiakshay-0D47A1?style=flat-square)](https://x.com/benganiakshay)
[![Email](https://img.shields.io/badge/akshaybengani@gmail.com-0D47A1?style=flat-square)](mailto:akshaybengani@gmail.com)

</div>

---

## What I'm building

Seven apps shipped this year across three platforms. Each one started because something
in my own life didn't have a tool, and every app I found solved a neighbouring problem
instead of the real one.

| Project | What it is | Built with |
| :--- | :--- | :--- |
| **[Hisaab](https://github.com/akshaybengani/Hisaab)** | A fully offline ledger for handing out things at cost and collecting the cash back. It isn't inventory, it tracks who owes you money and treats stock as a by-product. | Flutter · 416 tests |
| **[Medstock](https://github.com/akshaybengani/Medstock)** | An offline stock book for a household's medicines. Not a pill reminder, a logistics ledger: what's left, when it runs out, and what to order to reach a given date. | Flutter |
| **[MyPlaces](https://github.com/akshaybengani/MyPlaces)** | An offline field notebook for houses you visit on foot, for the half of the world whose address is a lane, a landmark, and a family name. | Flutter |
| **[Token Counter](https://github.com/akshaybengani/token-counter)** | Today's token spend across Claude Code, Codex, Gemini CLI, and Cursor, as a ring against a daily target you set. Reads files those tools already wrote to disk. | Swift · macOS |
| **[GitGlance](https://github.com/akshaybengani/gitglance)** | A menu bar dashboard for every git repo on your Mac. Not a git client, a guardrail: which repos have work sitting on a branch it should never have landed on. | Swift · macOS |
| **[Replay](https://github.com/akshaybengani/ReplayAutomation)** | A macOS menu bar macro recorder. Do a task by hand once, and it does it again while you go elsewhere. | Swift · 116 tests |
| **[Barge](https://github.com/akshaybengani/barge)** | A queue for file operations. Not a faster copier, a scheduler for copies that verifies what arrived matches what left before deleting an original. | Electron · TypeScript |

## The thread running through them

I keep arriving at the same four decisions, so they're worth stating once.

**No network unless the problem needs one.** Six of the seven make zero network calls. That
isn't a feature I added, it's a constraint I started from, and it removes accounts, sync
conflicts, outages, and the entire question of what happens to somebody's data.

**Derive state, never decrement it.** Medstock computes what's left from a snapshot plus
what's happened since, rather than mutating a running total. A counter that drifts is
impossible to audit. A derivation you can recompute is impossible to lose.

**The README is part of the build.** Every project opens with the problem in plain language
before it mentions a single feature, because a stranger gives you about one screen before
deciding.

**Tests are the finish line, not the intention.** Counts on the badges are real and they run.

## What I work in

**Mobile** · Flutter and Dart, since 2019. Offline-first architecture, local persistence, on-device media, Play Store releases.

**Desktop** · Swift and SwiftUI for macOS (menu bar apps, accessibility APIs, event tap recording, zero dependencies). Electron and TypeScript where it has to run on Windows too.

**AI engineering** · Python for LLM tooling: RAG over documents, multi-model playgrounds, provider wrappers, MCP servers, and agent workflows. I work with Claude Code daily and build the tooling around it.

**Before all of that** · Java and Android, Swift and UIKit, Node, React, Go, and a long stretch of Python automation. Most of it is still public in this account, which is why you'll find about a hundred repos behind the seven above.

## Currently

Engineering at **Pratham Softwares**, based in India. Building AI tooling by day and finishing the
list of small apps my family kept asking for by night.

<div align="center">

Ideas, or a project you think I'd enjoy? **[akshaybengani@gmail.com](mailto:akshaybengani@gmail.com)**

</div>
