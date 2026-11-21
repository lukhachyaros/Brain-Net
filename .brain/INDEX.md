# Project Brain Index
*Generated: 2026-11-21T07:20:42.400969+00:00*

## Description
<img src="docs/images/hero-banner.jpg" alt="Project Brain — Graph Memory for AI Coding Agents" width="100%">

## Main Modules
- **project-brain/** (7 files)
- **(root)/** (5 files)
- **.github/** (1 files)
- **tests/** (1 files)

## Central Nodes
- `file:project-brain/scripts/brain.py` (file, 15 links): Project Brain CLI now bootstraps scan and digest automatically during init, with skip-bootstrap and clean JSON output.
- `file:project-brain/SKILL.md` (file, 9 links): Lightweight runtime skill package with one-shot bootstrap; consumer setup copies only SKILL.md, brain.py, agent block, and viewer assets.
- `file:README.md` (file, 5 links): Main repository and installation documentation; consumer setup copies only runtime skill files and keeps tests, package README, and documentation images out.
- `file:project-brain/assets/agent-block.md` (file, 5 links): Injected agent block explicitly runs at every session start and does not require repeated skill invocation.
- `decision:20261121071955-slim-runtime-skill-package` (decision, 2 links): Consumer installations copy only SKILL.md, brain.py, agent-block.md, and viewer.html. Package README, documentation images, and test suite stay outside the runtime skill folder.
- `file:tests/test_brain.py` (file, 2 links): Development-only unittest suite with 76 tests; kept outside the runtime skill package.
- `decision:20261121071439-oneshot-persistent-project-setup` (decision, 2 links): The init command performs instruction injection, scan, and digest automatically; injected instructions persist activation across later sessions and --skip-bootstrap provides an escape hatch.
- `file:LICENSE` (file, 2 links): MIT license for the project-brain skill.
- `file:project-brain/assets/viewer.html` (file, 2 links): Self-contained force-directed graph viewer with Canvas rendering, dark/light theme, search, filters, timeline slider, and live polling.
- `decision:20261121070811-adaptive-budgeted-graph-retrieval` (decision, 2 links): Use adaptive graph depth and a token budget for query retrieval; superseded nodes are excluded and superseding decisions mark old records inactive.

## Recent Decisions
- **Slim runtime skill package** (`decision:20261121071955-slim-runtime-skill-package`): Consumer installations copy only SKILL.md, brain.py, agent-block.md, and viewer.html. Package README, documentation images, and test suite stay outside the runtime skill folder.
- **One-shot persistent project setup** (`decision:20261121071439-oneshot-persistent-project-setup`): The init command performs instruction injection, scan, and digest automatically; injected instructions persist activation across later sessions and --skip-bootstrap provides an escape hatch.
- **Adaptive budgeted graph retrieval** (`decision:20261121070811-adaptive-budgeted-graph-retrieval`): Use adaptive graph depth and a token budget for query retrieval; superseded nodes are excluded and superseding decisions mark old records inactive.
- **Rewrite README installation guidance** (`decision:20261121013819-rewrite-readme-installation-guidance`): Split skill installation from project initialization, add prerequisites, copy layout, Windows commands, verification, and clear agent locations.
- **Harden Brain-Net storage and CLI** (`decision:20261121011910-harden-brainnet-storage-and`): Advisory OS locks are authoritative; old lock files are retained, data records carry schema version, init supports safe preview and injection controls, and graph API supports bounded filtering.

## Stale Files (Need Re-reading)
- `file:.github/copilot-instructions.md` (.github/copilot-instructions.md)
- `file:AGENTS.md` (AGENTS.md)
- `file:GEMINI.md` (GEMINI.md)

## Nodes Needing Summary
- `file:.github/copilot-instructions.md` (.github/copilot-instructions.md)
- `file:AGENTS.md` (AGENTS.md)
- `file:GEMINI.md` (GEMINI.md)

## Open Tasks
- [ ] **Add more language parsers** (`task:20261120112604-add-more-language-parsers`): Consider adding Go, Rust, Java, C# import parsers for broader project support.
