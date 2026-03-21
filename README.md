# PM Project Brain

A reusable prompt that helps product managers set up persistent AI context ("project brain") for any AI coding assistant. Run it once, answer the interview questions, and your product knowledge, terminology, writing standards, and key decisions load automatically in every future conversation.

## What it does

The prompt walks you through four sections:

1. **Product Context**: vision, codenames, business models, customer segments, metrics, infrastructure, geographic footprint, features, active/paused initiatives
2. **Terminology & Acronyms**: product, technical, business, infrastructure, platform, and organizational terms — kept consistent everywhere
3. **Writing Standards**: document formats (PRFAQs, PRDs, one-pagers, etc.), writing voice, metric conventions, FAQ style, PRD templates, and formatting rules
4. **Key Decisions & Constraints**: settled strategic/product/technical/pricing decisions, things you don't do, canceled initiatives, and open questions

After the interview, the AI generates context files in the correct format for your tool.

## Supported tools

Kiro IDE / CLI · Claude Code · Gemini CLI · Antigravity · Codex CLI · Cursor · Windsurf

See the [compatibility table in the prompt](PM-Project-Brain-Prompt.md#compatible-tools-and-where-files-go) for file locations, global paths, and format details.

## How to use

1. Open the [prompt section of PM-Project-Brain-Prompt.md](PM-Project-Brain-Prompt.md#the-prompt)
2. Copy everything between the `START COPYING HERE` and `STOP COPYING HERE` delimiters
3. Paste it into your AI assistant and follow the interactive interview
4. Review the generated files and commit them to your project repo

The AI will ask which tool you're using and create files in the right format and location.

## Tips

See [Tips for providing input](PM-Project-Brain-Prompt.md#tips-for-providing-input) in the prompt file.