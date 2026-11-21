---
name: project-brain
description: Persistent graph memory for the current project. Use at the start of any session in a project, before reading or searching the codebase, after creating/editing/deleting files, and after design decisions or bug findings. Avoids re-reading the whole repo by keeping summarized nodes and links in .brain/.
---

# Project Brain

Run all commands from the project root. `BRAIN` = `python <this-skill-dir>/scripts/brain.py`.

## Bootstrap
If `.brain/` does not exist: run `BRAIN init`. Initialization is one-shot bootstrap: it injects the persistent instructions, scans the project, and generates `.brain/INDEX.md`. Summarize nodes flagged `needs_summary` with `BRAIN touch <path> --summary "..." --link ...`.
After bootstrap, do not ask the user to invoke this skill again; the injected instructions apply to later sessions in this project.

The runtime skill package is intentionally small: `SKILL.md`, `scripts/brain.py`, `assets/agent-block.md`, and `assets/viewer.html`. Do not copy README, documentation images, or test files into a consumer project.

## Every session
1. `BRAIN sync`. Read `.brain/INDEX.md` once, then only the files listed as stale/new. Do not run memory retrieval for every chat message.
2. Never scan or read the whole repo.

## While working
- For a task, locate context with `BRAIN query "<keywords>" --depth 0 --budget 2000` before opening files. `--depth 0` adapts exploration to match quality; `--budget` caps retrieval. Open a real file only if its node is stale or the summary is insufficient.
- After every file create/edit/delete: `BRAIN touch <path> --summary "<1-2 sentences>" --link <node_id>[:edge_type]`.
- After every design decision, bug, or change of direction: `BRAIN note --type decision|bug|thought|task --title ... --summary ... --link ...`. A decision replacing an older one uses `supersedes`.
- Every thought/decision node must link to at least one file or concept node.

## End of session
`BRAIN lint`, fix reported issues, then `BRAIN digest`.

## Viewer
`BRAIN serve` and open http://127.0.0.1:8765 when the user wants to see the graph.

## Rules
- Never hand-edit `.brain/nodes.jsonl` or `.brain/edges.jsonl`.
- Use `--json` when parsing output.
