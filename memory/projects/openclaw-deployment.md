# OpenClaw Deployment (Lyra + Persona Roster)

## Status
Active — expanding to multi-agent roster

## Started
2026-07-03

## Overview
Deploying OpenClaw as a personal assistant system with a main orchestrator, **Lyra**, as the Telegram interface (formerly "Clawdia" / "LadyClawdiaBot"), delegating to a named roster of sub-agent personas following a constellation/celestial naming scheme. Provider setup uses local Ollama (qwen3:14b on the Unraid RTX 3060) with Anthropic's API available as an alternative provider.

## Persona Roster

**Main orchestrator:**
- **Lyra** — main orchestrator / Telegram interface. See `IDENTITY.md`.

**Sub-agents** (see `personas/`):
- **Draco** — security watchdog (auth failures, intrusion alerts, cert expiry)
- **Corvus** — notifications/alerting messenger (Home Assistant, Uptime Kuma, service-down alerts)
- **Vela** — background task runner (scheduled jobs, backups, cron-driven work)
- **Polaris** — health-check/status agent (uptime, resource usage, status queries)
- **Cygnus** — media/arr-stack liaison (Sonarr/Radarr/Overseerr requests)
- **Auriga** — GPU/inference routing (Ollama vs Anthropic API, model selection)
- **Norma** — config management / infra-as-code agent
- **Phoenix** — recovery/restart agent (restarts failed containers)
- **Carina** — logging/observability aggregation

## Goals

1. Get the workspace (identity, memory, tools) into a clean, real starting state — done.
2. Stand up Lyra on Telegram as the primary interface.
3. Stand up the named sub-agent roster with clear scopes, following `docs/agent-architecture.md` and `docs/task-routing.md`.
4. Wire up homelab-manager capabilities (Unraid, UDM Pro network, self-hosted services) split across the relevant personas.
5. Decide routing between local Ollama and Anthropic API (Auriga's scope) depending on task sensitivity/complexity.
6. Decide whether each sub-agent gets its own bot identity/channel or all route through Lyra's single Telegram bot.

## Current Progress

### Completed
- [x] Repo scaffolding in place (SOUL.md, IDENTITY.md, USER.md, memory system)
- [x] Main orchestrator identity defined (Lyra, she/her)
- [x] Replaced demo/placeholder content with real data
- [x] Renamed from Clawdia/LadyClawdiaBot to Lyra throughout the workspace
- [x] Defined sub-agent persona roster and role scopes (`personas/`)

### In Progress
- [ ] Telegram bot wiring (Lyra)
- [ ] Provider routing (Ollama vs Anthropic) — Auriga
- [ ] Homelab tool integration (TOOLS.md specifics: hosts, services, VLANs)
- [ ] Deciding sub-agent bot/channel topology (one bot vs many)

### Backlog
- [ ] Heartbeat/monitoring tuned to real services, split across Draco/Corvus/Vela/Polaris
- [ ] Security tooling (outbound filter, audit log) wired into the Telegram flow
- [ ] Actual bot registration/deployment code (does not exist in this repo yet — this workspace is context/config only)

## Decisions

**2026-07-03**: Adopted constellation/celestial naming scheme for the full agent roster, replacing the single-assistant "Clawdia" identity and the "LadyClawdiaBot" Telegram name.
- Reason: Eric is expanding from one assistant to a fuller roster of task-specific personas; needed a coherent, extensible naming convention.
- Trade-off: More personas to keep coherent (voice, scope, memory) than a single assistant — mitigated by giving each a scoped, narrow role rather than a full personality like Lyra's.

## Next Actions

1. Fill in TOOLS.md with concrete SSH hosts/service endpoints for the homelab, mapped to the persona that owns each.
2. Confirm Telegram bot token/config and connect Lyra.
3. Decide default provider policy (local vs Anthropic) — Auriga's first real task.
4. Decide sub-agent bot/channel topology (single bot with persona-tagged replies vs. separate bot registrations).

---

*Last updated: 2026-07-03*
