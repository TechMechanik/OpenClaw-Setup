# Personas

Named sub-agent roster, delegated to by **Lyra** (main orchestrator — see `IDENTITY.md`). Constellation/celestial naming scheme.

Each persona file follows the same shape:

- **Role** — one-line scope
- **Reports to** — always Lyra, never Eric directly (per `docs/agent-architecture.md`'s communication rules)
- **Scope** — what it owns
- **Triggers** — when Lyra hands work to it
- **Allowed Actions** — what it can do without escalating back to Lyra/Eric
- **Escalation** — when it must hand back up
- **Notes** — open questions / TBD implementation details

See `docs/agent-architecture.md` for the overall delegation model and `docs/task-routing.md` for the routing table.

## Roster

| Persona | Role | Status | File |
|---------|------|--------|------|
| Draco | Security watchdog | Defined — not yet implemented | [draco.md](draco.md) |
| Corvus | Notifications/alerting messenger | Defined — not yet implemented | [corvus.md](corvus.md) |
| Vela | Background task runner | Defined — not yet implemented | [vela.md](vela.md) |
| Polaris | Health-check/status agent | Defined — not yet implemented | [polaris.md](polaris.md) |
| Cygnus | Media/arr-stack liaison | Defined — not yet implemented | [cygnus.md](cygnus.md) |
| Auriga | GPU/inference routing | Defined — not yet implemented | [auriga.md](auriga.md) |
| Norma | Config management / IaC | Defined — not yet implemented | [norma.md](norma.md) |
| Phoenix | Recovery/restart agent | Defined — not yet implemented | [phoenix.md](phoenix.md) |
| Carina | Logging/observability | Defined — not yet implemented | [carina.md](carina.md) |

## Open Architecture Question

Whether each persona gets its own Telegram bot registration (separate bot identities Eric can message directly) or all route through Lyra's single bot with persona-tagged replies is not yet decided — see `memory/projects/openclaw-deployment.md`. Nothing in this repo currently registers any bot; these files define scope and behavior only, for whichever transport is chosen.

---

*Last updated: 2026-07-03*
