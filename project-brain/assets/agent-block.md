<!-- BRAIN:START — managed by project-brain, do not edit this block -->
## Project Brain — Graph Memory

**All commands:** `python {{BRAIN_PATH}} <command>`

1. **At the start of every session:** run `sync`, then read `.brain/INDEX.md` once and only files listed as stale/new. This is automatic because Project Brain is initialized for the project; do not ask the user to invoke the skill again.
2. **Find task context:** run `query "<keywords>" --depth 0 --budget 2000` before opening files. `--depth 0` adapts graph depth; `--budget 2000` caps estimated context.
3. **After every file create/edit/delete:** run `touch <path> --summary "<1-2 sentences>" --link <node_id>[:edge_type]`.
4. **After every design decision, bug, or change of direction:** run `note --type decision|bug|thought|task --title "..." --summary "..." --link <node_id>[:edge_type]`. A decision replacing an older one must include `--link <old_decision_id>:supersedes`.
5. **End of session:** run `lint`, fix reported issues, then `digest`.
6. **Never** hand-edit `.brain/nodes.jsonl` or `.brain/edges.jsonl`.
<!-- BRAIN:END -->
