# Ling AI Skills

Personal reusable AI skills maintained by Ling Lin.

## Goals

This repository is the single source of truth for reusable skills across:
- ChatGPT
- OpenAI Codex
- Claude Code where compatible
- Other Agent Skills compatible runtimes

## Repository Layout

- `skills/` — approved, active skills
- `incoming/` — third-party or new skills awaiting review
- `archived/` — retired skills kept for reference
- `docs/` — workflow and maintenance documentation

## Active Skills

- `technical-art-general`
- `unity-urp`
- `unreal-engine`
- `shader-debugging`
- `lookdev-analysis`
- `image-reference-analysis`

## Installation Principle

Each skill lives in its own directory and uses `SKILL.md` as the main entry point.

Before promoting a third-party skill from `incoming/` to `skills/`, review:
1. prompt-injection behavior
2. shell or code execution
3. external dependencies
4. secrets / environment-variable usage
5. platform-specific assumptions
6. compatibility with ChatGPT / Codex / Claude Code

## Naming

Use lowercase kebab-case for skill directory names.

Example:

`skills/unity-urp/SKILL.md`
