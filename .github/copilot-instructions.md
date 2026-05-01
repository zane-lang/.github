# GitHub Copilot Instructions — zane-lang/.github

This repository is the **organization meta repo** for the Zane language GitHub org (templates, policy docs, shared workflows, etc.).

## 0) Non-negotiables (read first)
- **Do not invent language behavior or syntax.**
	- The **source of truth for Zane language design is the spec repo**: https://github.com/zane-lang/spec
	- When you need language details, cite / follow the spec documents (especially `syntax.md`) instead of guessing.
- Prefer **small, reviewable diffs** over large refactors.
- Keep changes **mechanical and reversible** (especially in CI/workflows).

## 1) Where things live (cross-repo map)
When asked to add or update content, put it in the repo that “owns” it:

- **Language design / semantics / syntax**
	- Repo: https://github.com/zane-lang/spec
	- Start from: `README.md` (inventory), then the relevant topic doc (e.g. `memory_model.md`, `purity.md`, `error_handling.md`, etc.), plus `syntax.md`.
- **Compiler**
	- Repo: https://github.com/zane-lang/compiler
- **Coda configuration format**
	- Repo: https://github.com/zane-lang/coda
- **Tree-sitter grammar for Coda**
	- Repo: https://github.com/zane-lang/tree-sitter-coda
- **Docs site content sourced by zane-lang.org**
	- Repo: https://github.com/zane-lang/docs
- **Website**
	- Repo: https://github.com/zane-lang/website

If a request is about language behavior but the change is being made here, your default action is:
- write a short note in the PR/comment pointing to the correct repo, and
- if asked to draft text/code anyway, draft it as a “proposed patch” targeting the correct repo.

## 2) Formatting & whitespace (tabs, with explicit exceptions)
### 2.1 Tabs are the default indentation
- Use **literal tab characters** (U+0009) for indentation in code.
- Use **one tab per indent level**.
- Do not convert tabs ↔ spaces in existing files unless the change is explicitly about formatting.

### 2.2 Exceptions (files where tabs are wrong or dangerous)
- **Documentation**: requires indenting with four spaces to display correctly on GitHub.
- **YAML** (`.yml`, `.yaml`): do **not** use tabs for indentation (use spaces).
- **Markdown lists** can be sensitive; keep existing indentation style if the renderer/layout matters.
- In any file with an established style, **match the local style**.

### 2.3 Trailing whitespace / newlines
- No trailing whitespace.
- End files with a single newline (`\n`).
- Prefer LF line endings.

## 3) Writing/Editing spec content (when you’re asked to help)
If you are asked to write or revise spec text, follow the spec repo’s conventions:
- Each topic has a **single canonical home document**; don’t duplicate rules across docs.
- Topic docs should follow the required “shape” (title, brief lead-in, optional “See also”, `---` separators, numbered headings, etc.).
- `syntax.md` defines **form** (surface syntax). Topic docs define **semantics**.

When drafting spec changes in chat:
- Provide a **ready-to-paste Markdown patch** (section headings included).
- Keep prose direct, rule-like, and testable.
- Include at least one **minimal code example** per non-obvious rule.
- Add cross-references instead of duplicating content.

## 4) Generating Zane code examples (only when requested)
- Treat `zane-lang/spec/syntax.md` as the canonical reference for surface syntax.
- Prefer minimal examples that demonstrate exactly one rule.
- If an example depends on semantics (ownership, effects, abort paths, concurrency), cross-check the relevant topic doc in the spec repo first.
- If you are unsure, explicitly say what you’re unsure about and point to the spec file/section you would verify.

## 5) Generating Coda examples (only when requested)
- Coda is **whitespace-sensitive** and **line-oriented**.
- Preserve comments and their placement.
- Be careful with table headers and the reserved keyword `key` in keyed tables.
- Use tabs for indentation in examples unless the surrounding file demands otherwise.

## 6) GitHub workflows, issue templates, and config in this repo
This repo will typically contain:
- GitHub issue templates / PR templates
- Shared GitHub Actions workflows
- Community health files

Rules of thumb:
- Prefer the simplest workflow that gets the job done.
- Pin action versions intentionally.
- Never print secrets.
- If changing CI behavior, update any related docs/comments in the same PR.

## 7) “Defaults you can edit” (maintainer knobs)
Edit this section to match the org’s preferences; Copilot should follow it once set.

- Preferred indentation:
	- Default: tabs
	- YAML: 2 spaces
- Preferred max line length:
	- TODO: set (e.g. 100/120)
- Preferred tone for docs:
	- TODO: set (e.g. “direct, technical, minimal fluff”)
- Preferred changelog style:
	- TODO: set
- Preferred commit/PR title convention:
	- TODO: set (e.g. Conventional Commits, or “area: summary”)
- Minimum supported toolchain versions (if any):
	- TODO: set

## 8) What to do when instructions conflict
Priority order:
1. The current repository’s local config/docs (CODEOWNERS, CONTRIBUTING, style guides, etc.)
2. These Copilot instructions
3. General best practices
