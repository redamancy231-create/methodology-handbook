> [中文版本](../README.md) | English | [正體中文](../zh-Hant/README.md)

# Methodology & Lessons Learned Handbook

**A compact, battle-tested companion to the AI Collaboration Full-Lifecycle Framework—50 empirically grounded lessons.**

Version 1.0 | 2026-07-18

> Its relationship to the full AI Collaboration Full-Lifecycle Framework (168K characters) is like that of a “textbook” and an “error logbook”: the framework presents the systematic methodology, while this handbook distills real-world mistakes into quick-reference entries. The two complement each other. The source material comes from the author’s personal notes; this handbook is the curated version prepared for public release.

---

## Contents

| Section | Entries | Coverage |
|---------|---------|----------|
| §1 Engineering Discipline | 9 | Verification and validation, cleanup and release, version management, code refactoring |
| §2 AI Collaboration Methodology | 32 | Multi-model review, provenance, prompt design, Workflow, cognitive biases |
| §3 File Formats and Tool Pitfalls | 6 | YAML/JSON, DOCX, text editing, encoding, configuration files |
| §4 Quantitative Research | 3 | Feature leakage, LambdaRank, regime detection |

Each entry contains a **title**, a one-sentence lesson, a key quote, an empirical date, and a category tag.

---

## Category Tag Index

| Tag | Meaning | Entries |
|-----|---------|---------|
| Verification Discipline | Independent verification after making claims or changing configurations or wording | 3 |
| Release Discipline | Cleanup, exclusion, and zero-residue confirmation before release | 3 |
| Version Management | The full synchronization scope of a version-number update | 1 |
| Code Refactoring | Methods for extracting modules from a monolith | 1 |
| Tool Usage | Conventions for sending instructions to external CLI tools | 1 |
| Multi-Model Review | Strategies for using multiple AI models to review code or documents | 9 |
| provenance | Tracing deliverables back to their source models | 3 |
| Independence Review | Preventing the same AI from occupying multiple roles | 1 |
| Tool Evaluation | Empirical methods for evaluating AI agent tools | 2 |
| Experimental Design | Effect sizes of prompt variation versus model variation | 1 |
| Task Execution | Execution discipline when following a plan and workflows for text generation | 2 |
| Deliverable Design | Pairing patterns for md/json deliverables | 1 |
| Prompt Design | Writing CLAUDE.md and designing Skills | 2 |
| Workflow | Task routing, cross-validation, and preservation of process files | 3 |
| Context Management | When to trigger large-context compression | 2 |
| Cognitive Bias | Optimistic self-assessment, overgeneralized empirical claims, and blind spots involving formatting residue | 3 |
| Collaboration Metacognition | Adversarial review, passive observation, and retry strategies after failures | 3 |
| File Formats | YAML/JSON/CFF/DOCX format pitfalls | 3 |
| Text Editing | Collateral damage from global replacement of short patterns | 1 |
| Encoding | Chinese character encoding in Windows terminals | 1 |
| Configuration | Confirming which configuration file the system actually reads | 1 |
| Quantitative Research | Feature leakage, LambdaRank sensitivity, and regime lag | 3 |

---

## Glossary

The handbook refers to several specific tools and Workflow concepts. Focus on the **general principles** in each entry—the principles do not depend on any particular CLI implementation.

| Term | Definition | Origin |
|------|------------|--------|
| Workflow | A multi-agent orchestration framework supporting parallel and pipeline-based subtask distribution | Claude Code CLI |
| agent() | The function used to start a sub-agent in Workflow | Claude Code CLI |
| headroom_compress | A tool that precompresses large amounts of text to conserve the context window | Claude Code CLI (MCP) |
| Safety classifier / classifier | A component that performs a safety review before commands are executed | Claude Code CLI |
| Codex CLI | OpenAI’s command-line AI programming tool | Codex CLI |
| [GATE] | A blocking point in a plan that requires human confirmation | Project planning convention |
| P0/P1/P2 | Priority levels: blocking/high/medium | General project management |
| zero-involvement | A reviewer did not participate in creating the material under review | Review methodology |
| provenance | A record tracing a deliverable to its model backend × session | General AI collaboration |

See the handbook appendix for the complete glossary.

---

## Audience & Prerequisites

**Target audience:** Developers and researchers who use AI programming tools such as Claude Code, Codex CLI, and Cursor for software engineering or academic projects. Basic experience with AI-assisted programming is assumed.

**Scope of evidence:** “Empirical” in this handbook refers to specific incidents recorded by the author across dozens of AI collaboration projects between May and July 2026. Numbers such as “7/7 convergence” and “~11% bias” come from individual observations. Their applicability is limited to the model versions and task types used at the time. They should be treated as **case references**, not statistical conclusions.

The handbook is published as an md/json pair. The md file is the source of truth and is generated before the json file.

---

## How to Use

**Browse, don’t read.** This is a reference handbook, not a tutorial. Navigate by category tag when you encounter a specific situation:

- Preparing a code review → §2.1 Multi-Model Review Strategies
- Preparing a project for release → §1.2 Cleanup and Release
- Troubleshooting configuration → §3.5 Configuration Files

---

## Format

- `方法论与经验教训手册.md` — Human-readable format, including the table of contents, anchor links, and glossary appendix
- `方法论与经验教训手册.json` — Machine-readable structured data organized as `metadata` → `sections[]` → `subsections[]` → `entries[]`

---

## License

CC-BY-4.0

---

## Author

[Acerolaorion](https://github.com/redamancy231-create)
