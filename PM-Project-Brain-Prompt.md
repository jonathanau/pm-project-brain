I am a product manager. I need you to help me build a "project brain," a set
of persistent context files that will load automatically in every future
conversation, so I never have to re-explain my product, terminology, decisions,
or writing standards.

We will create four context documents through an interactive interview. Ask me
the questions below one section at a time. After each section, show me the
draft for my review before moving to the next. I can provide answers directly,
or I can share documents (PRFAQs, PRDs, one-pagers, OP docs, strategy decks)
for you to extract the information from.

---

## Section 1: Product Context

Ask me about:
1. Product name, vision statement, and elevator pitch
2. Key project codenames and what they refer to
3. Business models (subscriptions, freemium, marketplace, ads, etc.)
4. Target customer segments with demographics and behavioral descriptions
5. Key metrics and their current values (include time period)
6. Technical infrastructure overview (what powers the product)
7. Geographic footprint (where it's live, where it's expanding)
8. Major features or product areas and their current status
9. Active projects and initiatives (with owner, status, key data points)
10. Paused initiatives and their expected restart criteria (so you never
    reference them as actively underway)

Output format: a markdown document titled "Product Context" with sections for
each area above. Use bullet points. Include specific numbers and dates wherever
possible. Flag paused initiatives in their own section.

---

## Section 2: Terminology & Acronyms

Ask me about:
1. Product and project names (correct capitalization, what NOT to call them)
2. Technical terms and acronyms specific to our product
3. Business terms and acronyms used in our metrics and reporting
4. Infrastructure terms
5. Device, platform, or distribution channel terms
6. Organizational and process terms (team names, review cadences, planning cycles)

Output format: a markdown document titled "Terminology & Acronyms" organized
by category. Each entry should have the acronym/term followed by a colon and
its definition. Add a header note: "ALWAYS use these terms consistently. Do not
substitute alternatives."

---

## Section 3: Writing Standards

Ask me about:
1. What document types does your team write? (e.g., PRFAQs, PRDs,
   one-pagers, strategy docs, OP docs) For each, what is the expected structure?
2. What is your team's writing voice? (e.g., data-driven, concise, narrative)
3. How do you refer to your team ("we") and your users ("customers")?
4. What are your conventions for presenting metrics? (time periods, abbreviations,
   precision)
5. How do you structure FAQs in documents?
6. Do you have a PRD template? If so, share it and I will extract the
   structure, section names, conventions for user stories, acceptance criteria
   format, metrics tables, and priority tiers.
7. Any general formatting rules? (tables vs. prose, appendix conventions, etc.)

Output format: a markdown document titled "Writing Standards" with sections for
Document Formats (with structural outlines for each type), Writing Style,
Metric Conventions, FAQ Style, and General Rules. If a PRD template was
provided, include a detailed "PRD Conventions" section.

---

## Section 4: Key Decisions & Constraints

Ask me about:
1. Strategic decisions that are settled and should not be revisited
   (e.g., "we are a freemium-first business")
2. Content or product decisions that constrain what we build
   (e.g., "all games must run on Linux")
3. Technical or infrastructure decisions
   (e.g., "we evaluated X and decided not to migrate")
4. Pricing and monetization decisions
5. Things we explicitly do NOT do (and why)
6. Canceled initiatives (with brief rationale)
7. Any open questions or decisions pending a deadline

Output format: a markdown document titled "Key Decisions & Constraints" with
a header note: "These are standing decisions and constraints. ALWAYS respect
these when generating content or recommendations." Organize by category. Include
a "Things We Do NOT Do" section and a "Canceled Initiatives" section.

---

## After all four sections are complete

1. Show me a summary of all four documents for final review.
2. Ask me which AI tool I am using (Kiro, Claude Code, Gemini CLI, Antigravity, Codex CLI, Cursor, GitHub Copilot, OpenCode, Qwen Code, Windsurf, or other).
3. Based on my answer, create the files in the correct format and location:

   **Kiro IDE or Kiro CLI:**
   Create four files in `.kiro/steering/`:
   - `product-context.md`
   - `terminology.md`
   - `writing-standards.md`
   - `decision-log.md`
   Each file needs this YAML front matter at the top:
   ```
   ---
   inclusion: always
   ---
   ```
   Then ask if I want them at the global level (`~/.kiro/steering/`) so they
   load in every workspace.

   **Claude Code:**
   Create or append to `CLAUDE.md` in the project root, using H1 headers
   to separate the four sections. For global context, also offer to create
   `~/.claude/CLAUDE.md`.

   **Gemini CLI:**
   Create or append to `GEMINI.md` in the project root, using H1 headers
   to separate the four sections. For global context, also offer to create
   `~/.gemini/GEMINI.md`.

   **Antigravity:**
   Create or append to `.gemini/GEMINI.md` in the project root, using H1
   headers to separate the four sections. For global context, also offer
   to create `~/.gemini/GEMINI.md`.

   **Codex CLI:**
   Create or append to `AGENTS.md` in the project root, using H1 headers
   to separate the four sections. For global context, also offer to create
   `~/.codex/AGENTS.md`.

   **Cursor:**
   Create four `.mdc` files in `.cursor/rules/`:
   - `product-context.mdc`
   - `terminology.mdc`
   - `writing-standards.mdc`
   - `decision-log.mdc`
   Each file needs this YAML front matter:
   ```
   ---
   description: <brief description>
   globs:
   alwaysApply: true
   ---
   ```

   **GitHub Copilot:**
   Create or append to `.github/copilot-instructions.md` in the project root,
   using H1 headers to separate the four sections. For global context, instruct
   the user to add the content to their account or organization settings under
   Copilot > Custom Instructions.

   **OpenCode:**
   Create or append to `AGENTS.md` in the project root, using H1 headers
   to separate the four sections. For global context, also offer to create
   `~/.config/opencode/AGENTS.md`.

   **Qwen Code:**
   Create or append to `QWEN.md` in the project root (or `.qwen/QWEN.md`),
   using H1 headers to separate the four sections. For global context,
   also offer to create `~/.qwen/QWEN.md`.

   **Windsurf:**
   Create four `.md` files in `.windsurf/rules/`:
   - `product-context.md`
   - `terminology.md`
   - `writing-standards.md`
   - `decision-log.md`
   Each file must be under 12,000 characters. At the top of each file,
   add a comment indicating activation mode:
   ```
   <!-- Activation: Always On -->
   ```
   For global rules, offer to add the content to `global_rules.md` via
   Windsurf Settings > Cascade Memories > Global Rules.

   **Other / generic:**
   Create four markdown files in a `.ai/context/` directory and instruct
   the user to reference them in their tool's configuration. (`.ai/context/`
   is a suggested convention; adjust the path if your tool expects files
   elsewhere.)

4. Remind me that I can update these files anytime by asking the AI to make
   changes, and that I should review them quarterly to keep them current.
