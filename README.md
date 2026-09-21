<div align="center">

# Akshay Bengani

**I build agent systems for work, and finish the software I need at home.**

MCP servers and evaluation harnesses by day. A Rust audio hub, an on-device agent runtime, and a rack-less wall of hardware by night.

[![Website](https://img.shields.io/badge/akshaybengani.com-0D47A1?style=flat-square)](https://akshaybengani.com/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0D47A1?style=flat-square)](https://www.linkedin.com/in/akshaybengani/)
[![X](https://img.shields.io/badge/@benganiakshay-0D47A1?style=flat-square)](https://x.com/benganiakshay)
[![Medium](https://img.shields.io/badge/Medium-0D47A1?style=flat-square)](https://medium.com/@akshaybengani)
[![Email](https://img.shields.io/badge/akshaybengani@gmail.com-0D47A1?style=flat-square)](mailto:akshaybengani@gmail.com)

</div>

---

## What I'm building

Four systems, all private while they settle. The write-ups on
[akshaybengani.com](https://akshaybengani.com/) are the way in.

### Hermes and the self-hosted AI stack
**A personal agent running on my own hardware, with a hard boundary around what it can touch.**
Every model call goes through a gateway holding five virtual keys, split by what the caller is
for rather than who it is. Access fails closed, and tool restriction is enforced where tools are
registered rather than on the key, so a client cannot discover or call anything outside its
envelope no matter what it sends.

The most useful thing it taught me: **tool surface compounds model weakness.** One MCP server
exposes 87 tools, another 104. Handing all of them to a weaker model doesn't make it more
capable, it makes it fail harder, because the size of the choice grows faster than the ability to
make it. The fix isn't a better model, it's several narrow registrations against the same
upstream server. Same server, different doors.

Seventeen containers on one mini PC, behind a firewall load balancing two ISPs.

### SoundA2Z
**A control plane for the audio you already own.** Per-app volume, sample-accurate multi-room
zones, and one API an assistant can actually drive. Rust, 9 crates, 112,000 lines, 689 tests.

Give a model a volume setter and it loops calls to fake a fade, and it stutters, because a model
round trip takes a second or two while an audio ramp needs a tick every 20 milliseconds. So every
setter takes a fade duration and there are no relative setters at all. Clients send intent; one
ticker in the hub owns the clock. An assistant can't get the timing wrong if it never holds the
timing.

Hub and agent split over gRPC, three OS audio backends, a simulator crate so the hub is testable
with no audio hardware present, and Snapcast supervised as a process and deliberately never
linked, because that boundary is a licensing decision rather than a technical one.

### MYOCA
**Make your own chat agent.** A bring-your-own-key Android agent runtime with no backend and no
login, where each agent is granted device capabilities one at a time. Flutter, 89,000 lines, 677
tests, 11 feature modules. Keys, chats and documents never leave the phone, which is a constraint
the architecture has to earn rather than a promise in a policy.

### HomeBook
**A memory of the house.** Search "drill", get back Park Street, ground floor, garage, tool
cabinet, drawer 2. Flutter, 83,000 lines, 1,295 tests. Accounts and sharing live in Firebase; what
is actually in your house lives where you choose, which is a hosted tier, your own server, or the
phone and nowhere else.

## Built to solve one specific problem

| Project | The problem |
| :--- | :--- |
| **[Medstock](https://github.com/akshaybengani/Medstock)** | A thousand pills a month for three generations, and no way to know what's left or what to order. Not a pill reminder, a logistics ledger where stock is derived from a snapshot and never decremented. |
| **[Barge](https://github.com/akshaybengani/barge)** | Copying four folders at once to a home NAS made all four crawl, and one would hang at 99%. A queue that runs one transfer at a time and verifies what arrived matches what left before deleting any original. |
| **[Replay](https://github.com/akshaybengani/ReplayAutomation)** | GUI chores no API could reach. A macOS recorder that replays real clicks and keystrokes, built on the accessibility and event tap APIs, and readable afterwards. |

Also public, and smaller: [Hisaab](https://github.com/akshaybengani/Hisaab) (an offline debt
ledger), [Token Counter](https://github.com/akshaybengani/token-counter) (daily AI token spend as
a desktop ring), [GitGlance](https://github.com/akshaybengani/gitglance) (a menu bar warning when
a repo has work on the wrong branch), and
[MyPlaces](https://github.com/akshaybengani/MyPlaces) (an offline field notebook for
door-to-door visits).

## The day job

Implementation and technical enablement on an enterprise agent platform, which in practice means
building the thing and then proving it works.

**MCP servers in production.** Built and deployed servers backing a live alerting system, from
scoping through deployment, QA and handover. Along the way I found two protocol defects that had
left both servers unusable by any compliant client, because the tests mocked the transport
instead of speaking it.

**Evaluation, not assertion.** A probe runner and two 43 case batteries, measuring detection
rates across configurations. An agent that sounds right and an agent that is right are different
claims, and only one of them survives a battery.

**The unglamorous half.** Production escalations root caused and shipped, runbooks, QA reports,
and the occasional load bearing claim withdrawn once I'd found I couldn't support it.

## What I work in

**Systems I've architected** · Rust (a distributed hub and agent over gRPC, real-time scheduling, three OS audio backends), Swift for macOS down to the accessibility and event tap APIs, Electron where it has to run on Windows too. I specify these, review every decision, and debug them when they break. The code is written with AI, which is the same discipline I apply professionally: ask me why the audio hub owns the clock rather than the client, not to recite Rust syntax.

**AI and agents** · MCP server development on both sides of the protocol, agent evaluation and probe batteries, RAG with LangChain and FAISS, LangGraph, Google ADK, multi-agent orchestration.

**Languages I work in daily** · Dart and Flutter since 2019, Python, TypeScript. Offline-first architecture, local persistence, on-device media, Play Store releases. Before that, a PCI-DSS compliant fintech platform for under-18s.

**Infrastructure** · Proxmox and LXC, pfSense, Docker, Cloudflare Tunnel, Home Assistant, and currently Kubernetes. I run a homelab that everything above gets tested on first.

**Before all of that** · Java and Android, Swift and UIKit, Node, React, Go, and a long stretch of Python automation. Most of it is still public in this account, which is why there are about a hundred repos behind the ones above.

## Writing

Fifteen pieces on [Medium](https://medium.com/@akshaybengani), mostly written the evening after I
got something working, while I still remembered what had gone wrong. Proxmox and TrueNAS, Home
Assistant automations, a three part account of putting solar on the house, and what it actually
delivered.

<div align="center">

More at **[akshaybengani.com](https://akshaybengani.com/)** · Ideas, or a project you think I'd enjoy? **[akshaybengani@gmail.com](mailto:akshaybengani@gmail.com)**

</div>
