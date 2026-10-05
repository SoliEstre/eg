# EG OS

**A meta-harness for your agents.** It runs *with* whatever harness each of your agents already uses — never instead of one. The stable edition of [EstreGenesis](https://github.com/SoliEstre/EstreGenesis), and the meta-harness Observatory (`ov.estre.so`) provides and recommends.

See [EDITION.md](EDITION.md) for exactly what this edition contains and which upstream commit it was built from.

---

## Five minutes

You do not install a platform. You give your agent one file.

1. **Copy one seed** into your project — start with `AI_Native_Project_Seed_Prompt_Compact.md`.
2. **Point your agent at it.** It reads the seed and writes an `AGENTS.md` for *your* project — your stack, your conventions, your constraints.
3. **That's the whole first step.** From here your agent has a durable place to keep what it learns about your codebase, instead of relearning it every session.

Nothing above requires a server, a plugin, or an account.

When you want more, add modules one at a time:

```
/plugin marketplace add SoliEstre/eg
/plugin install estregenesis@eg-os
```

Each module is independent. Install one, some, or none.

---

## Where it sits

| Layer | What it is |
|---|---|
| **Firmware** | The model and the vendor's own harness or cloud runtime — Claude Code, Codex, Grok, Antigravity, a vendor-hosted cloud agent. It boots one agent and runs its tools. |
| **Buses** | The open protocols agents speak to tools and to each other — MCP, A2A. |
| **EG OS** | The layer above, where several agents — often from several vendors — work on one thing. |
| **Your project** | What the work is for. |

Vendors keep absorbing what used to need a layer like this: agents in one account can already message each other, and delegation inside one runtime is native. What they do not give you is the part EG OS is built around — **you can read what your agents say to each other**, decisions wait for you instead of travelling inside a message, and the state of the work outlives any one vendor. That is why EG OS goes *with* your harnesses rather than competing with them: the more agents and vendors you run, the more there is to see.

**Agents that live in a vendor's cloud** — a persistent cloud computer, a hosted agent session — join as autonomous peers acting for you, not as workers. That path is specified and not yet open: the board's MCP channel runs over stdio only, and a board on your own machine cannot be reached from a vendor's cloud. Serving boards so that it can — and giving you one place to watch and decide across them — is what Observatory (`ov.estre.so`) is being built for. It is in development.

---

## What it manages

"OS" is a claim, so here is what it means concretely. An operating system arbitrates scarce resources between processes. For coding agents the scarce resource is **context**, and the rest follows:

| An OS manages | EG OS's counterpart |
|---|---|
| CPU time, scheduling | **Superscalar** — how many lanes to fan out, and what each lane runs on |
| Memory | **Context** — surviving compaction, handoff cards, brief tiering |
| Inter-process communication | **Constellation** — where agent-to-agent conversation is observed, decided and recorded; native channels may carry it, the board sees it |
| Device drivers | **Harness adapters** — the seat contract (Pantty) and per-harness bindings, so each vendor's runtime plugs in the same way |
| Persistent storage | **Compendium** vocabulary store · board state · durable lessons |
| Permissions, protection rings | Decision gates, escalation rubric, **Ultrasafe** review |
| Package management | This marketplace · plugins · seed tiers |

Context is to agents what memory was to early operating systems: the thing you run out of first, and the thing everything else is designed around.

---

## What this is not

**It is not small.** Seven module specifications, eight plugins, a live board server, MCP servers. Calling that lightweight would set an expectation that breaks on contact.

The honest framing is **a large system with a small first step** — the same relationship you have with any OS. You do not learn all of it to run one command.

**It is not a framework you import.** Most of EG OS is convention, specification and discipline that your agent reads. The runtime parts are optional and additive.

---

## Editions and upgrades

Editions are dated and cut **weekly**: `2026.08.1` is August's first edition, `2026.08.2` its second. One edition is a set of module versions that were verified together and then left alone.

Weekly is chosen to match how people actually switch between work, maintenance and side projects — an edition is roughly the unit of "what I picked up this week".

Between editions, these do not break without a migration note: seed markers and tier names, plugin ids and skill names, and the board wire contract (additive changes only). Section numbers inside specifications and internal runtime structure carry no such promise. The full policy is in [COMPATIBILITY.md](COMPATIBILITY.md).

If you want the newest work instead of the verified composition, use the upstream repository directly — it moves several times a day, and that is the trade.

---

## Upstream

Development happens in [EstreGenesis](https://github.com/SoliEstre/EstreGenesis): specifications, the reference runtime, the checkers, and the dogfooding record. This repository is **composed** from it — every file here is extracted from a single upstream commit. Do not send patches here; send them upstream.

Apache-2.0.
