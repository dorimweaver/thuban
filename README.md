# Thuban · 右枢

English · [中文](README.zh-CN.md)

**Your repo has a memory problem. Thuban gives it a spine.**

Every new agent session starts from zero. It re-reads half the codebase, guesses which doc is current, and confidently follows instructions that went stale last month. Thuban is a skill that fixes the *project*, not the agent: it organizes structure, important documents, and context routes so that both people and agents can pick up any task without archaeology.

## What it does

| You say | It does |
|---|---|
| `thuban` / `右枢` | A full local governance pass: understand the project, repair stale instructions and broken routes, tidy directories and documents, verify the result |
| `thuban this subproject` | The same, scoped to one area, checking only the parent routes it affects |
| `thuban, read-only` | Inspect and recommend, change nothing |

## How it thinks

- **One owner per truth.** Every fact or rule lives in exactly one document; everything else links to it. Owner documents say under their title what they own and how to maintain them, so they get rewritten instead of growing into date-stamped logs.
- **Nodes grow from real work.** A `THUBAN.md` gateway appears only where independent ongoing work and local context justify it, and merges back when that value disappears. No standard tree, no document quota.
- **Routes, not essays.** Each node tells the next reader *when* to open *which* file and *what* it contributes.
- **Humans count too.** The README-level map stays in sync with the routing, so a person can see the whole project at a glance.
- **Verified, then stable.** Changes are checked against routes, meaning, operations, and recovery; a second pass on a healthy project produces zero diff.

```text
AGENTS.md → THUBAN.md (root)
              ├─ area/THUBAN.md → local docs and operating guides
              └─ README / architecture / important-file map
```

## Package

| File | Role |
|---|---|
| [SKILL.md](SKILL.md) | Invocation, scope and authorization, core judgments |
| [references/GOVERNANCE.md](references/GOVERNANCE.md) | Full governance, organizing, verification |
| [references/THUBAN-PROTOCOL.md](references/THUBAN-PROTOCOL.md) | Nodes, routes, growth, startup, maintenance contract |
| [references/COMPATIBILITY.md](references/COMPATIBILITY.md) | Recognizing and migrating older versions |

## Install

Clone into your user skill directory, for example:

```bash
git clone https://github.com/dorimweaver/thuban ~/.agents/skills/thuban
```

Any agent host that discovers skills from `SKILL.md` can use it. Updating the skill never rewrites a project by itself; projects change only when you run a governance pass.

## License

[MIT](LICENSE) © 2026 Dorim Weaver
