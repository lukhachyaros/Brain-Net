# Project Brain Index
*Generated: 2026-11-21T01:41:37.549807+00:00*

## Description
<img src="docs/images/hero-banner.jpg" alt="Project Brain — Graph Memory for AI Coding Agents" width="100%">

## Main Modules
- **project-brain/** (6 files)
- **(root)/** (5 files)
- **.github/** (1 files)

## Central Nodes
- `file:project-brain/scripts/brain.py` (file, 11 links): Core CLI implementation; improved lock safety, schema versioning, init options, API filtering, gitignore matching, and automatic compaction.
- `file:project-brain/README.md` (file, 5 links): Concise skill-level README with quick start, install locations, commands, viewer, data files, and requirements.
- `file:README.md` (file, 4 links): Main project README with architecture, installation, agent setup, CLI, storage, testing, and license documentation.
- `file:project-brain/scripts/test_brain.py` (file, 4 links): Regression test suite for CLI, graph storage, locking, init, compact, query, and diagnostics.
- `file:project-brain/assets/agent-block.md` (file, 4 links): Injected agent instruction block with 6 rules for brain-aware AI coding sessions.
- `file:project-brain/SKILL.md` (file, 4 links): Agent skill definition with bootstrap, session, and working instructions for AI coding agents.
- `decision:20261121013819-rewrite-readme-installation-guidance` (decision, 2 links): Split skill installation from project initialization, add prerequisites, copy layout, Windows commands, verification, and clear agent locations.
- `file:LICENSE` (file, 2 links): MIT license for the project-brain skill.
- `decision:20261120112603-use-jsonl-appendonly-format` (decision, 2 links): JSONL chosen for git-friendly diffs, atomic appends, and simple conflict resolution via last-write-wins.
- `file:project-brain/assets/viewer.html` (file, 2 links): Self-contained force-directed graph viewer with Canvas rendering, dark/light theme, search, filters, timeline slider, and live polling.

## Recent Decisions
- **Rewrite README installation guidance** (`decision:20261121013819-rewrite-readme-installation-guidance`): Split skill installation from project initialization, add prerequisites, copy layout, Windows commands, verification, and clear agent locations.
- **Harden Brain-Net storage and CLI** (`decision:20261121011910-harden-brainnet-storage-and`): Advisory OS locks are authoritative; old lock files are retained, data records carry schema version, init supports safe preview and injection controls, and graph API supports bounded filtering.
- **stdlib only, zero dependencies** (`decision:20261120112604-stdlib-only-zero-dependencies`): No pip install required. All functionality built on Python 3.10+ standard library for maximum portability.
- **Canvas over SVG for rendering** (`decision:20261120112603-canvas-over-svg-for`): HTML Canvas chosen over SVG for force-directed graph rendering to handle 1000+ nodes without DOM overhead.
- **Use JSONL append-only format** (`decision:20261120112603-use-jsonl-appendonly-format`): JSONL chosen for git-friendly diffs, atomic appends, and simple conflict resolution via last-write-wins.

## Stale Files (Need Re-reading)
- None. All indexed files are fresh.

## Nodes Needing Summary
- None. All nodes are summarized.

## Open Tasks
- [ ] **Add more language parsers** (`task:20261120112604-add-more-language-parsers`): Consider adding Go, Rust, Java, C# import parsers for broader project support.
