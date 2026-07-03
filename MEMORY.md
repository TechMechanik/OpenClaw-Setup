# MEMORY.md — Index

> This is a lightweight reference table. Detail lives in linked files.
> Load this every session (~1-2k tokens). Drill into detail files only when needed.

---

## ⚠️ Active Context (always load in main session)
These files contain critical ongoing context. Load at session start.
- `memory/people/user.md` — Eric, always relevant
- `memory/projects/openclaw-deployment.md` — Current active project (this workspace's own setup)

## 👤 People

| Name | Role | Last Contact | Detail | Triggers |
|------|------|--------------|--------|----------|
| Eric Stoddard | Human/Principal | 2026-07-03 | [user.md](memory/people/user.md) | eric, user, boss, human |

## 📁 Projects

| Project | Status | Updated | Detail | Triggers |
|---------|--------|---------|--------|----------|
| OpenClaw Deployment | Active | 2026-07-03 | [openclaw-deployment.md](memory/projects/openclaw-deployment.md) | openclaw, clawdia, telegram, ladyclawdiabot, ollama |
| Linux Desktop Rebuild | Planning | 2026-07-03 | [linux-desktop-rebuild.md](memory/projects/linux-desktop-rebuild.md) | linux, ubuntu, desktop, rebuild |
| UUFFXBG Technology Committee | Active | 2026-07-03 | [uuffxbg-tech-committee.md](memory/projects/uuffxbg-tech-committee.md) | uuffxbg, google workspace, tech committee |
| Photography Lens Roadmap | Active | 2026-07-03 | [photography-lens-roadmap.md](memory/projects/photography-lens-roadmap.md) | photography, lens, sony, lightroom |

## 📋 Recent Decisions (last 30 days)

| Date | Decision | Detail |
|------|----------|--------|
| 2026-07-03 | Replaced OpenClaw demo/template content with real starting dataset | This session |

## 🔧 Active Preferences
- Communication: direct, low-formality, no corporate boilerplate.
- Units: metric.
- External actions (sending, publishing, purchases): always ask first, no exceptions.
- Internal actions (reading, organizing, editing, config/install/update/remove for a clearly stated objective): proceed without asking.

## 🧠 Drill-Down Rules
1. **Conversation mentions a person?** → Load their people/ file
2. **Working on a project?** → Load its projects/ file
3. **Making a decision?** → Check decisions/ for precedent
4. **Unsure about context?** → Use memory_search or vector memory
5. **Session start:** Always load Active Context files (max 2-3)
6. **Hard cap:** Max 5 drill-downs at session start

## 📂 Other Reference Files

| File | What |
|------|------|
| memory/accounts.md | Service accounts and platforms |
| memory/pending-tasks.md | Open tasks |
| docs/agent-architecture.md | Multi-agent architecture |
| docs/task-routing.md | Delegation rules |
| docs/morning-brief-template.md | Morning brief structure |

## 🗄️ Daily Logs
Raw daily logs live in `memory/YYYY-MM-DD.md`. These are append-only journals.
Only load when you need specific detail about what happened on a particular day.
No daily logs exist yet — this workspace's real history starts 2026-07-03.

---

*Last updated: 2026-07-03*
*Update this index whenever you update a detail file. Same commit. No exceptions.*
