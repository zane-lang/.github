# Zane Roadmap

A high-level view of where the [Zane](https://github.com/zane-lang) ecosystem
is and where it's headed. This tracks major milestones across repositories, not
every task — each repo's own issues are the source of truth for detail.

Legend: `[x]` done · `[~]` in progress · `[ ]` planned

## Language & format

- [x] **Language specification** — [`spec`](https://github.com/zane-lang/spec)
  - [x] Foundations
  - [x] Type system
  - [x] Runtime model
  - [x] Program structure
- [x] **Coda configuration format** — [`coda`](https://github.com/zane-lang/coda)
  - [x] Format specification
  - [x] Reference implementation
  - [x] Bindings (Python, C++, C FFI, OCaml)

## Compiler — [`compiler`](https://github.com/zane-lang/compiler)

- [~] **Compiler & CLI**
  - [ ] Concrete syntax tree (CST)
  - [ ] Typed AST
  - [ ] Code emission
  - [ ] Diagnostics & error reporting

## Standard packages

Packages provided by Zane itself.

- [ ] `core` — the minimal core package
- [ ] `std` — the standard library

## Tooling & ecosystem

- [~] **Editor & language support**
  - [x] Tree-sitter grammar for Coda — [`tree-sitter-coda`](https://github.com/zane-lang/tree-sitter-coda)
  - [~] LSP
- [~] **Developer tooling**
  - [~] `checkpoint` CLI utility — [`checkpoint`](https://github.com/zane-lang/checkpoint)
- [~] **Project presence**
  - [~] Website — [`website`](https://github.com/zane-lang/website)
  - [~] Documentation — [`docs`](https://github.com/zane-lang/docs)
  - [x] Brand & logos — [`logos`](https://github.com/zane-lang/logos)
  - [x] Organization profile & community health files — [`.github`](https://github.com/zane-lang/.github)

## Contributing

Interested in helping move an item forward? See
[CONTRIBUTING.md](CONTRIBUTING.md) and pick up an issue on the relevant
repository.
