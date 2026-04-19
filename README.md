# PM Project Brain

A reusable prompt that helps product managers set up persistent AI context ("project brain") for any AI coding assistant. Run it once, answer the interview questions, and your product knowledge, terminology, writing standards, and key decisions load automatically in every future conversation.

## What it does

The prompt walks you through four sections:

1. **Product Context**: vision, codenames, business models, customer segments, metrics, infrastructure, geographic footprint, features, active/paused initiatives
2. **Terminology & Acronyms**: product, technical, business, infrastructure, platform, and organizational terms, kept consistent everywhere
3. **Writing Standards**: document formats like PRFAQs (press release/FAQs), PRDs (product requirements documents), and one-pagers; writing voice; metric conventions; frequently asked questions (FAQ) style; PRD templates; and formatting rules
4. **Key Decisions & Constraints**: settled strategic/product/technical/pricing decisions, things you don't do, canceled initiatives, and open questions

After the interview, the AI generates context files in the correct format for your tool.

## Compatible tools and where files go

| Tool | Context file location | Global location | Format |
|---|---|---|---|
| Claude Code | `CLAUDE.md` (project root) | `~/.claude/CLAUDE.md` | Single markdown file |
| Codex CLI | `AGENTS.md` (project root) | `~/.codex/AGENTS.md` | Single markdown file |
| Antigravity | `.gemini/GEMINI.md` (project root) | `~/.gemini/GEMINI.md` | Single markdown file (same as Gemini CLI) |
| Gemini CLI | `GEMINI.md` (project root) | `~/.gemini/GEMINI.md` | Single markdown file |
| Cursor | `.cursor/rules/*.mdc` | User-level rules in Settings | Markdown with YAML front matter |
| GitHub Copilot | `.github/copilot-instructions.md` | Settings > Copilot > Custom Instructions | Single markdown file |
| OpenCode | `AGENTS.md` (project root) | `~/.config/opencode/AGENTS.md` | Single markdown file |
| Qwen Code | `QWEN.md` (project root or `.qwen/QWEN.md`) | `~/.qwen/QWEN.md` | Single markdown file |
| Windsurf | `.windsurf/rules/*.md` | `global_rules.md` via Settings | Markdown (12K char limit per file) |
| Kiro IDE / CLI | `.kiro/steering/*.md` | `~/.kiro/steering/*.md` | Markdown with YAML front matter |

For single-file tools (Claude Code, Codex CLI, Gemini CLI, Antigravity, GitHub Copilot, OpenCode, Qwen Code), the AI will combine all sections into one file using H1 headers as separators. For multi-file tools (Kiro, Cursor, Windsurf), it will create one file per section.

## How to use

1. Copy the entire contents of [PM-Project-Brain-Prompt.md](PM-Project-Brain-Prompt.md?plain=1)
2. Paste it into your AI assistant and follow the interactive interview
3. Review the generated files and commit them to your project repo

The AI will ask which tool you're using and create files in the right format and location.

## Tips for providing input

- You can answer the questions conversationally, or you can share documents (drag and drop, paste, or reference files) and the AI will extract the relevant information.
- The more specific you are with numbers, dates, and names, the more useful the project brain will be.
- You do not need to answer every question. Skip what is not relevant and you can always add more later.
- Review your project brain quarterly to keep it current.

## License

This project is licensed under the [MIT License](LICENSE).