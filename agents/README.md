# Makabi OS — Agents Directory

> Per-agent specification files. One file per agent. ~128 in total across 15 departments.

## How this is organized

```
agents/
├── office-of-founder/    (4 — Massimo, Sunny, Reuben, Tamar)
├── engineering/          (14 — Luca + 13 specialists)
├── sales/                (10 — Vincenzo + 9 specialists)
├── marketing/            (13 — Raffaele + 12 specialists)
├── customer-success/     (9  — Giulia + 8 specialists)
├── operations/           (8  — Sofia + 7 specialists)
├── finance/              (10 — Marco + 9 specialists)
├── legal/                (8  — Shimon + 7 specialists)
├── people/               (6  — Eliana + 5 specialists)
├── voice/                (9  — Davide + 8 specialists, includes LOREN persona)
├── data/                 (7  — Naomi + 6 specialists)
├── real-estate/          (12 — Eitan + 11 specialists)
├── capital-markets/      (7  — Avi + 6 specialists)
├── quality-risk/         (6  — Yoni + 5 specialists)
└── brand-personas/       (5  — Loren-Persona, Maor, BRiXIE, Proprio, MaorEdit)
```

## How to use

Each `.md` file is a lightweight role definition that an agent can load via Memory protocol. The filename matches the agent slug (`massimo.md`, `aria.md`, `tania.md`).

To invoke an agent in any Claude session:

> "Aria, run outbound on the medspa list."

Or to load a specific agent's protocol:

```
Makabi Memory:get_protocol(name="agent-aria")
```

(Protocol auto-syncs from these files via the Massimo deploy hook.)

## Bulk install on any machine

Clone the repo and the agent files mirror to your local Claude Code project's `.claude/agents/` directory:

```bash
git clone https://github.com/michaelmakabi/makabi-os-agents.git
cp -r makabi-os-agents/agents/* ~/.claude/agents/
```

Or use the standalone tarball: [makabi-os-agents-bundle.tar.gz](../releases/latest)

## Master roster

See the [main README](../README.md) for the full chart and the [CHEAT-SHEET](../CHEAT-SHEET.md) for fast task-to-agent lookup.

## Source of truth

The canonical roster lives in Makabi Memory under protocol `makabi-os-agent-roster`. These files are the human-readable mirror.

---

*Powered by LOREN AI*
