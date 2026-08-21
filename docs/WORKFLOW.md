# Skill Intake and Installation Workflow

## Standard command

When Ling says:

> 安装这个 skill

Interpret it as the following workflow:

1. Read the supplied `SKILL.md` and supporting files.
2. Identify the original runtime (Claude Code, Codex, ChatGPT, generic Agent Skills, etc.).
3. Review for unsafe or overly broad instructions.
4. Review shell commands, scripts, network access, dependencies, and secrets usage.
5. Preserve useful behavior while removing unnecessary runtime-specific assumptions.
6. Normalize the skill into this repository's structure.
7. Place unreviewed material under `incoming/`.
8. After review, promote it to `skills/<skill-name>/`.
9. Update the root README if the active-skill list changes.
10. Commit changes with a concise message.

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

## Security

Never silently:
- execute downloaded binaries
- expose secrets
- upload private data
- alter unrelated repositories
- grant broader permissions
