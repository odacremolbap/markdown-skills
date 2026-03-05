# Markdown Diagrams Skill

A reusable skill that teaches AI coding agents how to create well-aligned diagrams and visual elements in Markdown files. Covers Mermaid diagrams, Unicode box-drawing, and lightweight rendered alternatives.

## What It Does

When installed, this skill provides guidelines for:

- **Mermaid diagrams** — 20+ diagram types with syntax reference, best practices, and layout control (flowcharts, sequence diagrams, class diagrams, ER diagrams, Gantt charts, C4, and more)
- **Unicode box-drawing** — precise character-level diagrams with alignment rules and verification checklists
- **Lightweight rendered diagrams** — js-sequence and flowchart.js for simple cases
- **Choosing the right approach** — decision guidance for when to use each tool

## Installation

### Claude Code

Install from the skill marketplace:

```
/install-skill https://github.com/odacremolbap/markdown-skills
```

Or add it manually to your project's `.claude/settings.json`:

```json
{
  "skills": [
    "https://github.com/odacremolbap/markdown-skills"
  ]
}
```

### Other Agents

The skill is defined in [`SKILL.md`](SKILL.md) at the repo root. To use it with any AI coding agent that supports system prompts or custom instructions:

1. Copy the contents of `SKILL.md` (skip the YAML frontmatter between the `---` delimiters)
2. Add it to your agent's system prompt, custom instructions, or rules file

Common locations by agent:

| Agent | Where to add |
|-------|-------------|
| Cursor | `.cursor/rules/*.md` or `.cursorrules` |
| Windsurf | `.windsurfrules` |
| Cline | `.clinerules` |
| Aider | `.aider.conf.yml` under `read` |
| Continue | `.continue/rules/*.md` |
| GitHub Copilot | `.github/copilot-instructions.md` |

### Manual / Generic

If your agent doesn't support file-based rules, paste the content of `SKILL.md` directly into the system prompt or conversation context before asking the agent to create diagrams.

## Usage

Once installed, the skill activates automatically when you ask the agent to create or fix diagrams, flowcharts, or ASCII art in Markdown files. You can also invoke it explicitly:

- In Claude Code: `/markdown-diagrams`
- In other agents: reference the rules file or include a prompt like _"follow the markdown diagram guidelines"_

## License

Apache 2.0 — see [LICENSE](LICENSE).
