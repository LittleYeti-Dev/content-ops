# Content Ops — NSQ Content Lab

**Yeti Knowledge Systems** · Persona: **Feed Crusher**

Content signal processing engine and social media operations layer for [Non Sequitur](https://github.com/LittleYeti-Dev/non-sequitur-web).

## What This Repo Does

Feed Crusher pulls daily feeds (X, LinkedIn, IG, RSS, Gunther DCR signals), triages signals with Yeti, develops write candidates through a structured pipeline, and publishes to social channels.

## Pipeline

```
Signal → Assess → Draft → Shape → Refine → Package → Queue → Publish
```

## Repo Structure

```
.cowork.md                  ← Cowork project config (workspace mount requirement)
.taskmaster/                ← Persona, boot context, standing orders
  ├── personas/feed-crusher.md
  ├── project-instructions.md
  ├── boot-context.md
  └── status/               ← Session-end status cache (write-only)
signals/                    ← Signal assessments
pipeline/                   ← Content in development
social/                     ← Social post drafts by platform
  ├── x/
  ├── linkedin/
  └── ig/
metrics/                    ← Engagement tracking and analytics
white-paper/                ← HGC³AE² framework
  ├── hgc3ae2-framework.md
  └── sprint/               ← Sprint artifacts and outputs
```

## Coordination

| Agent | Role | Interface |
|-------|------|-----------|
| Gunther | Signals intake via DCR Section 8 | GitHub issues → `section-8-signal` label |
| Taskmaster | Sprint orchestration, deploy coordination | `.taskmaster/status/`, milestones |
| Claude Code | CLI publishing, Hugo builds, deploys | `social/` directory, branches |

## Links

- [NSQ Web Platform](https://github.com/LittleYeti-Dev/non-sequitur-web)
- [YKS Hub](https://github.com/LittleYeti-Dev/yks-hub)
- [Gunther (Chief of Staff)](https://github.com/LittleYeti-Dev/gunther)
