# OpenClaw Deployment (Clawdia / LadyClawdiaBot)

## Status
Active — initial setup

## Started
2026-07-03

## Overview
Deploying OpenClaw as a personal assistant ("Clawdia") with a Telegram bot front end (LadyClawdiaBot), acting as a homelab manager. Provider setup uses local Ollama (qwen3:14b on the Unraid RTX 3060) with Anthropic's API available as an alternative provider.

## Goals

1. Get the workspace (identity, memory, tools) into a clean, real starting state — not demo/placeholder data.
2. Stand up LadyClawdiaBot on Telegram as the primary interface.
3. Wire up homelab-manager capabilities (Unraid, UDM Pro network, self-hosted services).
4. Decide routing between local Ollama and Anthropic API depending on task sensitivity/complexity.

## Current Progress

### Completed
- [x] Repo scaffolding in place (SOUL.md, IDENTITY.md, USER.md, memory system)
- [x] Assistant identity defined (Clawdia, she/her)
- [x] Replaced demo/placeholder content with real data

### In Progress
- [ ] Telegram bot wiring (LadyClawdiaBot)
- [ ] Provider routing (Ollama vs Anthropic)
- [ ] Homelab tool integration (TOOLS.md specifics: hosts, services, VLANs)

### Backlog
- [ ] Heartbeat/monitoring tuned to real services (Unraid, UDM Pro, self-hosted stack)
- [ ] Security tooling (outbound filter, audit log) wired into the Telegram flow

## Next Actions

1. Fill in TOOLS.md with concrete SSH hosts/service endpoints for the homelab.
2. Confirm Telegram bot token/config and connect LadyClawdiaBot.
3. Decide default provider policy (local vs Anthropic) for cost/privacy tradeoffs.

---

*Last updated: 2026-07-03*
