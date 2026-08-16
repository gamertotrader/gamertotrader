# gamertotrader

**I build AI agents that run on hardware I own, and the guardrails that stop them breaking things.**

Most of what I publish is the stopping layer, not the demo. An agent that can edit its own
guardrail file has no guardrail.

---

### Out now

**[GGT](https://github.com/gamertotrader/GGT)** — three guardrails for AI coding agents.
Standard library only, no install step, MIT. Each one was extracted from a working system,
stripped of every path and name specific to it, and then **proven in a repository it had never
seen before it was published**.

|                     | Stops                                                                             | Proof            |
| ------------------- | --------------------------------------------------------------------------------- | ---------------- |
| `canon-guard`       | a shell command writing to a file you declared off-limits, without blocking reads | 8/8 foreign repo |
| `rbm-gate`          | a file operation whose plan does not carry the file's real SHA-256                | 9/9 foreign repo |
| `multi-agent-lanes` | N agent sessions overwriting each other in one working tree                       | 9/9 foreign repo |

Clone it and run `prove_foreign.py` yourself. Every number on that page came from a command
whose output was read.

---

### How I work

- **Measure before claiming.** "No error" is not "works". If a command can settle it, run the command.
- **Break it on purpose before trusting it.** `rbm-gate` contains no filesystem removal call of any
  kind, and a test reads its own source and fails the build if one ever appears. Deletion is
  absent, not discouraged.
- **State the limit in the README**, not in production. A tool that overclaims is worse than no
  tool, because people stop checking it.

---

### More soon

Several projects are still private while I get them to the same bar as the one above:

- **Alice / AGAIHAOS** — an autonomous agent meant to run 24/7 on my own machine first, a private
  server next, and offline on a phone after that. Getting something to run continuously is a
  different problem from getting it to run once.
- **GRAND STAND** — the Python and FastAPI runtime underneath it, so the agent is a real always-on
  process instead of a chat window I have to open.
- **The Law Set** — written rules the agent has to follow: read the file before claiming what is in
  it, cite the source, never delete anything. I wrote most of them after it did the opposite.

They ship when they can survive a stranger cloning them cold. Same bar as GGT.

---

### Reach me

[GitHub](https://github.com/gamertotrader) · [GGT](https://github.com/gamertotrader/GGT)
