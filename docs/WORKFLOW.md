# Skill Intake and Installation Workflow

The canonical implementation of this workflow is `skills/skill-installer/SKILL.md`.

## Standard command

When Ling says:

> 安装这个 skill

Interpret it as the following workflow:

1. Read the supplied `SKILL.md` and supporting files.
2. Identify the original runtime (Claude Code, Codex, ChatGPT, generic Agent Skills, etc.).
3. Review for unsafe or overly broad instructions.
4. Review shell commands, scripts, network access, dependencies, and secrets usage.
5. Review privacy risks because this repository is public.
6. Review provenance and redistribution/license constraints for third-party material.
7. Compare the incoming skill with existing skills to avoid duplication.
8. Preserve useful behavior while removing unnecessary runtime-specific assumptions.
9. Normalize the skill into this repository's structure.
10. Place uncertain or unreviewed material under `incoming/` when needed.
11. After review, install it under `skills/<skill-name>/` or merge it into the best existing skill.
12. Update the root README if the active-skill list changes.
13. Commit changes with a concise message.

## Update command

When Ling says:

> 更新 <skill-name> skill

Read the current skill first, preserve intentional behavior, then make a targeted revision.

## Archive command

When Ling says:

> 卸载 <skill-name> skill

Move the skill to `archived/` rather than deleting it permanently unless Ling explicitly asks for deletion.

## Compatibility

Prefer portable wording:
- "available shell" instead of "Claude Bash tool"
- "available file-reading capability" instead of vendor-specific read tools
- explicit requirements instead of assuming a particular MCP or connector exists

## Security and Privacy

Never silently:
- execute downloaded binaries
- expose secrets
- upload private data
- publish proprietary or employer-confidential content
- alter unrelated repositories
- grant broader permissions

For third-party skills, verify provenance and redistribution rights before copying substantial content into this public repository.
