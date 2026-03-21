# PM Project Brain

A reusable prompt that helps product managers set up persistent AI context ("project brain") for any AI coding assistant. Run it once, answer the interview questions, and your product knowledge, terminology, writing standards, and key decisions load automatically in every future conversation.

## What it does

The prompt walks you through four sections:

1. **Product Context**: vision, metrics, infrastructure, active/canceled initiatives
2. **Terminology & Acronyms**: consistent naming across your team
3. **Writing Standards**: document formats, voice, metric conventions
4. **Decision Log**: settled decisions, constraints, things you don't do

After the interview, the AI generates context files in the correct format for your tool.

## Supported tools

| Tool | Context location | Format |
|---|---|---|
| Kiro IDE / CLI | `.kiro/steering/*.md` | Markdown with YAML front matter |
| Claude Code | `CLAUDE.md` | Single markdown file |
| Gemini CLI | `GEMINI.md` | Single markdown file |
| Antigravity | `.gemini/GEMINI.md` | Single markdown file |
| Codex CLI | `AGENTS.md` | Single markdown file |
| Cursor | `.cursor/rules/*.mdc` | Markdown with YAML front matter |
| Windsurf | `.windsurf/rules/*.md` | Markdown (12K char limit per file) |

## How to use

1. Open [PM-Project-Brain-Prompt.md](PM-Project-Brain-Prompt.md)
2. Copy the section between the `START COPYING HERE` and `STOP COPYING HERE` delimiters
3. Paste it into your AI assistant and follow the interactive interview
4. Review the generated files and commit them to your project repo

The AI will ask which tool you're using and create files in the right format and location.

## Tips

- You can answer questions conversationally or share existing documents for the AI to extract from
- Skip questions that aren't relevant; you can always add more later
- Review your project brain quarterly to keep it current