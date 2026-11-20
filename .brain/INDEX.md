# Project Brain Index
*Generated: 2026-11-20T11:37:24.158577+00:00*

## Description
<img src="docs/images/hero-banner.jpg" alt="Project Brain — Graph Memory for AI Coding Agents" width="100%">

## Main Modules
- **project-brain/** (6 files)
- **(root)/** (5 files)
- **.github/** (1 files)

## Central Nodes
- `file:project-brain/scripts/brain.py` (file, 9 links): Core CLI tool with 14 commands for graph memory management. Handles JSONL storage, file locking, import parsing, and HTTP server.
- `file:project-brain/assets/agent-block.md` (file, 4 links): Injected agent instruction block with 6 rules for brain-aware AI coding sessions.
- `file:project-brain/SKILL.md` (file, 4 links): Agent skill definition with bootstrap, session, and working instructions for AI coding agents.
- `file:project-brain/scripts/test_brain.py` (file, 4 links): Comprehensive test suite with 69 tests across 12 categories. Covers parsers, sync, atomic writes, locking, digest, init, query, root detection.
- `file:project-brain/README.md` (file, 2 links): Skill documentation with quick start, tool compatibility table, command cheatsheet, and visual guide.
- `file:LICENSE` (file, 2 links): MIT license for the project-brain skill.
- `file:project-brain/assets/viewer.html` (file, 2 links): Self-contained force-directed graph viewer with Canvas rendering, dark/light theme, search, filters, timeline slider, and live polling.
- `file:.github/copilot-instructions.md` (file, 1 links): GitHub Copilot custom instructions containing the project-brain managed block.
- `file:GEMINI.md` (file, 1 links): Gemini CLI / Antigravity instruction file containing the project-brain managed block.
- `file:AGENTS.md` (file, 1 links): Agent instruction file for Codex and Antigravity, containing the project-brain managed block.

## Recent Decisions
- **stdlib only, zero dependencies** (`decision:20261120112604-stdlib-only-zero-dependencies`): No pip install required. All functionality built on Python 3.10+ standard library for maximum portability.
- **Canvas over SVG for rendering** (`decision:20261120112603-canvas-over-svg-for`): HTML Canvas chosen over SVG for force-directed graph rendering to handle 1000+ nodes without DOM overhead.
- **Use JSONL append-only format** (`decision:20261120112603-use-jsonl-appendonly-format`): JSONL chosen for git-friendly diffs, atomic appends, and simple conflict resolution via last-write-wins.

## Stale Files (Need Re-reading)
- None. All indexed files are fresh.

## Nodes Needing Summary
- None. All nodes are summarized.

## Open Tasks
- [ ] **Add more language parsers** (`task:20261120112604-add-more-language-parsers`): Consider adding Go, Rust, Java, C# import parsers for broader project support.
