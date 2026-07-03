# Task Routing Playbook

## Decision Framework

### Keep Work With Lyra When:
- Simple, quick tasks (< 5 min)
- Personal context needed (Eric's preferences, history)
- Real-time conversation with Eric
- Security-sensitive decisions requiring Eric's sign-off
- Tasks requiring Eric's approval

### Delegate to a Persona When:
- The task falls cleanly within one persona's defined scope (see `personas/`)
- Deep focus needed for > 15 min in that domain
- Task can be clearly bounded
- Lyra needs to stay responsive to Eric

## Quick Reference

| Scenario | Persona |
|----------|---------|
| Auth failures, intrusion alerts, cert expiry | Draco |
| Home Assistant / Uptime Kuma alert needs relaying | Corvus |
| Scheduled job, backup, cron-driven work | Vela |
| "Is X up?" / resource usage / status query | Polaris |
| Sonarr/Radarr/Overseerr request | Cygnus |
| Ollama vs Anthropic API routing | Auriga |
| Homelab config change / drift check | Norma |
| Restart a failed container/service | Phoenix |
| Log aggregation / "has this happened before?" | Carina |
| Anything personal, ambiguous, or needing Eric's judgment | Lyra (keep local) |

## Handoff Checklist
Before delegating to a persona:
- [ ] Task clearly falls in that persona's documented scope (`personas/<name>.md`)
- [ ] Success criteria are explicit
- [ ] Context needed is documented
- [ ] Escalation triggers for this specific task are noted, even if the persona's default escalation rules would normally cover it

## Receiving Results
When a persona returns:
- [ ] Verify completeness against its scope
- [ ] Check against acceptance criteria
- [ ] Integrate into Lyra's context
- [ ] Report to Eric in Lyra's voice
- [ ] Don't just forward raw persona output — Eric only ever hears from Lyra
