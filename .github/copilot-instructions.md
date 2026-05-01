# GitHub Copilot Instructions — zane-lang/.github

This repository is the **organization meta repo** for the Zane language GitHub org (templates, policy docs, shared workflows, etc.).

## 0) Non-negotiables (read first)
- **Do not invent language behavior or syntax.**
    - The **source of truth for Zane language design is the spec repo**: https://github.com/zane-lang/spec
    - When you need language details, cite / follow the spec documents (especially `syntax.md`) instead of guessing.
- Prefer **small, reviewable diffs** over large refactors.
- Keep changes **mechanical and reversible** (especially in CI/workflows).

## 1) Repo standards come from `contributing/` (always check first)
Before making changes in any repo:
- **Read `contributing/` first** (this is the canonical place for repo-specific standards).
- Then check other local guidance files if present (examples: `CONTRIBUTING.md`, `CODEOWNERS`, `README.md`, `STYLEGUIDE.md`, `.editorconfig`).
- When working across repos, **apply the standards of the target repo** (not this one).

If there is a conflict:
1. The current repository’s local docs/config (especially `contributing/`)
2. These Copilot instructions
3. General best practices

## 2) Where things live (cross-repo map)
When asked to add or update content, put it in the repo that “owns” it:

- **Language design / semantics / syntax**
    - Repo: https://github.com/zane-lang/spec
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

## 3) Formatting & whitespace (tabs, with explicit exceptions)
### 3.1 Tabs are the default indentation (for code and code-like formats)
- Use **literal tab characters** (U+0009) for indentation in code.
- Use **one tab per indent level**.
- Do not convert tabs ↔ spaces in existing files unless the change is explicitly about formatting.

### 3.2 Exceptions (files where tabs are wrong or dangerous)
- **Documentation (Markdown, etc.)**: use **four spaces** when indentation is required for correct rendering on GitHub.
    - Prefer fenced code blocks (```), and within fenced code blocks continue indenting with **four spaces**
- **YAML** (`.yml`, `.yaml`): do **not** use tabs for indentation (use spaces).
- **Markdown lists** can be sensitive; keep existing indentation style if the renderer/layout matters.
- In any file with an established style, **match the local style**.

### 3.3 Trailing whitespace / newlines
- No trailing whitespace.
- End files with a single newline (`\n`).
- Prefer LF line endings.

## 4) “Defaults you can edit” (maintainer knobs)
Edit this section to match the org’s preferences; Copilot should follow it once set.

- Preferred indentation:
    - Code: tabs
    - YAML: 2 spaces
    - Markdown indentation (when required for rendering): 4 spaces
- Preferred changelog style:
    - `CHANGELOG.md` using **Keep a Changelog** (curated entries; maintain `Unreleased`; release sections use SemVer tags)
    - Categories per section: `Added`, `Changed`, `Deprecated`, `Removed`, `Fixed`, `Security`
    - GitHub Releases can supplement with auto-generated PR lists, but `CHANGELOG.md` is the source of truth
- Preferred commit/PR title convention:
    - **Conventional Commits** for PR titles (squash-merge so the PR title becomes the commit message)
    - Format: `<type>(optional scope): <summary>` — use `!` / `BREAKING CHANGE:` footer for breaking changes
    - Allowed types: `feat` `fix` `docs` `refactor` `perf` `test` `build` `ci` `chore` `revert` `style`
    - Scopes for this repo: `ci`, `templates`, `policy`, `community`, `meta`
