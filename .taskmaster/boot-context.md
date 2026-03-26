# Boot Context — Content Ops (Feed Crusher)

> **Static reference data only.** No issue counts, no sprint positions, no dynamic state.
> All dynamic state comes from the GitHub API, live, every boot.

---

## Repo Identity

- **Repo:** `content-ops`
- **Owner:** LittleYeti-Dev
- **Purpose:** Content Lab for Non Sequitur (NSQ) — signal processing, content development, white paper management
- **Persona:** Feed Crusher
- **Parent project:** Yeti Knowledge Systems (YKS)

---

## Architecture

### Content Pipeline
```
Signal (Gunther DCR §8) → Intake (content-ops issue) → Assess → Draft → Shape → Refine → Package → Queue → Publish (NSQ)
```

### Signal Sources
- **Section 8:** X/Twitter feed signals triaged by Gunther's Daily Command Review
- **Section 9:** RSS feed sweep (queued — not yet implemented in Gunther's DCR prompt)
- **Ad hoc:** Yeti can inject signals from any source (IG, Grok, memory, conversation)

### Issue Labels
- `section-8-signal` — Signal from Gunther's X feed triage
- `section-9-signal` — Signal from RSS sweep (future)
- `content` — General content item
- `priority-critical` — Needs immediate attention
- `needs-yeti` — Blocked on Yeti decision
- `pipeline-draft` / `pipeline-shape` / `pipeline-refine` / `pipeline-queue` / `pipeline-published` — Pipeline stage tracking

---

## Key Assets in This Repo

- `white-paper/` — HGC³AE² framework ("Mitigating Confident Misalignment in Agentic Systems"). All AI capability signals should cross-reference this.
- `signals/` — Signal assessment docs (written by Feed Crusher)
- `pipeline/` — Content in development
- `.taskmaster/` — Persona configs, boot context, status cache

---

## YKS Repo Map (for cross-project awareness)

| Repo | Purpose | Feed Crusher Relevance |
|------|---------|----------------------|
| content-ops | This repo — Content Lab | HOME |
| non-sequitur-web | NSQ web platform (Hugo + Cloudflare Pages) | Publish target |
| gunther | Chief of Staff — DCR, Priority Board | Signal source, coordination |
| yks-hub | Central ops hub — personas, prompts, project management | Architecture reference |
| robo-stack | Infra code — Terraform, K8s, CI/CD | Content about infra topics |
| Agentics-Alistair-Prime | Alistair Prime task engine | Content about agentics |
| alistars-stack | Alistair cognitive runtime | Content about AI architecture |
| the-foremans-build-stack | Agentics framework docs | Architecture reference |
| the-markdown | WordPress production (archive) | Historical reference only |

---

## Coordination Model: Hub-Spoke via API

Feed Crusher does NOT clone other repos. It reads cross-project state via GitHub API (PAT) at boot:

1. **Gunther daily log** — Latest daily from `Chief of Staff/{week}/` for DCR context
2. **Gunther Priority Board** — `Chief of Staff/Priority_Board.md` for deadline awareness
3. **Gunther Action Items** — `Chief of Staff/ACTION_ITEMS.md` for cross-project blockers
4. **All repo milestones** — Sprint state across the portfolio
5. **Content-ops issues** — Live intake queue

This gives Feed Crusher full situational awareness without cross-repo cloning.

---

## Dual-Agent Architecture

- **Cowork (this session):** Planning, content development, signal assessment, issue management
- **Claude Code (Yeti's laptop):** Infra deploys, Hugo builds, Wrangler pushes, anything requiring persistent local state
- **Handoff mechanism:** GitHub (branches, issues, .taskmaster/ files)

---

## What NOT to Put Here

Do NOT add issue counts, sprint positions, pipeline state, or any dynamic data to this file.
This is static reference. Dynamic state lives in GitHub issues and is pulled live at every boot.
