<div align="center">

# Akshay Bengani

**I build agent systems for work, and finish the software I need at home.**

MCP servers and evaluation harnesses by day. A Rust audio hub, an agent runtime, and a house's memory by night.

[![Website](https://img.shields.io/badge/akshaybengani.com-0D47A1?style=flat-square)](https://akshaybengani.com/)
[![X](https://img.shields.io/badge/@benganiakshay-0D47A1?style=flat-square)](https://x.com/benganiakshay)
[![Email](https://img.shields.io/badge/akshaybengani@gmail.com-0D47A1?style=flat-square)](mailto:akshaybengani@gmail.com)

</div>

---

## What I'm building

Three systems, all still private while they settle. They're the work I'd want read first.

### SoundA2Z
**A control plane for the audio you already own.** Per-app volume, sample-accurate multi-room
zones, and one API an assistant can actually drive. Rust, 9 crates, 95,000 lines, 541 tests.

The design problem is worth stating. Give a model a volume setter and it loops calls to fake a
fade, which stutters, because a model round trip takes a second or two and an audio ramp needs
a tick every 20 milliseconds. So every setter in the API takes a fade duration and there are no
relative setters at all. Clients send intent; one ticker in the hub owns the clock and runs
every in-flight ramp on an equal-power curve. An assistant can't get the timing wrong if it
never holds the timing.

A hub and agent split over gRPC, three OS audio backends (PipeWire, Core Audio through a Swift
helper, WASAPI), a simulator crate so the hub is testable with no audio hardware present, and
Snapcast supervised as a process and deliberately never linked, because synchronized group
playback is patent-dense and that boundary is a licensing decision rather than a technical one.

### MYOCA
**Make your own chat agent.** A bring-your-own-key Android agent runtime with no backend and no
login, where each agent is granted device capabilities one at a time. Flutter, 54,000 lines,
461 tests, 11 feature modules.

Three provider adapters, an MCP client, per-agent permission scoping, and secure credential
storage. Keys, chats, and documents never leave the phone, which is a constraint the
architecture has to earn rather than a promise in a privacy policy.

### HomeBook
**A memory of the house.** Search "drill", get back Park Street, ground floor, garage, tool
cabinet, drawer 2. Flutter, 44,000 lines, 742 tests.

Local-first with a shared identity layer: your account and who you share a house with live in
Firebase, but what's actually in the house lives where you choose, which is our cloud, your own
server, or this phone and nowhere else.

## Built to solve one specific problem

Smaller, each one a single irritation followed all the way to a finished app.

| Project | The problem |
| :--- | :--- |
| **[Medstock](https://github.com/akshaybengani/Medstock)** | A thousand pills a month for three generations, and no way to know what's left or what to order. Not a pill reminder, a logistics ledger where stock is derived from a snapshot and never decremented. |
| **[Barge](https://github.com/akshaybengani/barge)** | Copying four folders at once to a home NAS made all four crawl, and one would hang at 99%. A queue that runs one transfer at a time and verifies what arrived matches what left before deleting any original. |
| **[Replay](https://github.com/akshaybengani/ReplayAutomation)** | GUI chores no API could reach. A macOS recorder that replays real clicks and keystrokes, built on the accessibility and event tap APIs, and readable and editable afterwards. |

Also public, and smaller still: [Hisaab](https://github.com/akshaybengani/Hisaab) (an offline
debt ledger), [Token Counter](https://github.com/akshaybengani/token-counter) (daily AI token
spend as a desktop ring), [GitGlance](https://github.com/akshaybengani/gitglance) (a menu bar
warning when a repo has work on the wrong branch), and
[MyPlaces](https://github.com/akshaybengani/MyPlaces) (an offline field notebook for
door-to-door visits).

## The day job: agent systems

I work in implementation and technical enablement on an enterprise agent platform, which in
practice means building the thing and then proving it works.

**MCP servers in production.** Built and deployed servers backing a live alerting system, from
scoping through deployment, QA, and handover. Along the way I found two protocol defects that
had left both servers unusable by any compliant client, because the tests mocked the transport
instead of speaking it.

**Evaluation, not assertion.** A probe runner and two 43 case batteries, measuring detection
rates across configurations. An agent that sounds right and an agent that is right are
different claims, and only one of them survives a battery.

**The unglamorous half.** Production escalations root caused and shipped, runbooks, QA reports,
and the occasional load bearing claim withdrawn once I'd found I couldn't support it.

## What I work in

**Systems** · Rust (distributed hub and agent over gRPC, real-time scheduling, cross-platform OS audio). Swift and SwiftUI for macOS, down to the accessibility and event tap APIs. Electron where it has to run on Windows too.

**AI and agents** · MCP server development on both sides of the protocol, agent evaluation and probe batteries, RAG with LangChain and FAISS, LangGraph, Google ADK, multi-agent orchestration.

**Mobile** · Flutter and Dart since 2019. Offline-first architecture, local persistence, on-device media, Play Store releases. Before that, a PCI-DSS compliant fintech platform for under-18s.

**Before all of that** · Java and Android, Swift and UIKit, Node, React, Go, and a long stretch of Python automation. Most of it is still public in this account, which is why there are about a hundred repos behind the ones above.

<div align="center">

Ideas, or a project you think I'd enjoy? **[akshaybengani@gmail.com](mailto:akshaybengani@gmail.com)**

</div>
