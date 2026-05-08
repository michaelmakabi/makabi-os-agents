# Bulk Agent Files — Install Bundle

> The canonical role definitions for all ~128 agents in one tarball.
> One-shot install on any machine via `git clone` + `cp`.

## Quick install

```bash
git clone https://github.com/michaelmakabi/makabi-os-agents.git
cd makabi-os-agents
mkdir -p ~/.claude/agents
cp -r agents/* ~/.claude/agents/
```

After this, every Claude Code session on that machine sees all agents. Invoke any one by name; the agent's role file is read at spawn time.

## What the bundle gives you

- `agents/office-of-founder/` — Massimo, Sunny, Reuben, Tamar
- `agents/engineering/` — Luca + 13 specialists (Beni, Gideon, Moshe, Ari, Yael, Bruno, Gabriel, Dante, Enzo, Fiorella, Niccolò, Tommaso, Ezra)
- `agents/sales/` — Vincenzo + 9 specialists
- `agents/marketing/` — Raffaele + 12 specialists
- `agents/customer-success/` — Giulia + 8 specialists (incl. Sage, Maya, Nova, Kira)
- `agents/operations/` — Sofia + 7 specialists
- `agents/finance/` — Marco + 9 specialists
- `agents/legal/` — Shimon + 7 specialists
- `agents/people/` — Eliana + 5 specialists
- `agents/voice/` — Davide + 8 specialists (incl. LOREN persona)
- `agents/data/` — Naomi + 6 specialists
- `agents/real-estate/` — Eitan + 11 specialists
- `agents/capital-markets/` — Avi + 6 specialists
- `agents/quality-risk/` — Yoni + 5 specialists
- `agents/brand-personas/` — Loren-Persona, Maor, BRiXIE, Proprio, MaorEdit

## File format

Each `.md` file follows a strict template:

```markdown
# AGENT_NAME

> Role · Reports to · Name origin

## What AGENT_NAME does
(role description)

## Tools at AGENT_NAME's disposal
(tool list)

## Default protocols loaded
(memory protocols auto-loaded on spawn)

## How to invoke
(example invocation phrases)

## Escalation
(specialist → dept head → Massimo → Master Makabi)

## Hard rules
(memory discipline, brand rules, etc.)
```

## Sync with Memory

Each file's role is also stored in Makabi Memory as protocol `agent-<slug>`. The two stay in sync via the deploy hook in this repo.

To pull the latest from Memory:

```bash
# (script lives in tools/sync-from-memory.sh — to be added)
```

To push local changes back to Memory:

```bash
# (script lives in tools/push-to-memory.sh — to be added)
```

## What's already pushed inline

The most important agents (MASSIMO, SUNNY, REUBEN, TAMAR, plus all 13 Department Heads) are committed individually as full-fat specification files in `agents/<dept>/<name>.md`. The remaining specialists are in the bundle tarball — same content, just packaged for fast install.

---

*Powered by LOREN AI*
