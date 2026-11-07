# Zane Roadmap

A high-level view of where the [Zane](https://github.com/zane-lang) ecosystem
is and where it's headed. This tracks major milestones across repositories, not
every task — each repo's own issues are the source of truth for detail.

Legend: `[x]` done · `[~]` in progress · `[ ]` planned · `[-]` paused

## Language & format

- [x] **Language specification** — [`spec`](https://github.com/zane-lang/spec)
  - [x] Foundations
  - [x] Type system and runtime model: types, generics, memory, lifetimes, effects, concurrency
  - [x] Program structure: control flow, errors, packages, dependencies
  - [x] Calling C (`ffi.md`) and math intrinsics (`math.md`)
  - [x] A design story for every spec document
- [~] **Spec and compiler in step** — the compiler records where it differs
  from the spec in
  [`docs/spec-divergences.md`](https://github.com/zane-lang/compiler/blob/main/docs/spec-divergences.md);
  the two are reconciled once the syntax settles
- [x] **Coda configuration format** — [`coda`](https://github.com/zane-lang/coda)
  - [x] Format specification
  - [x] Reference implementation (header-only C++)
  - [x] Bindings: Python (on PyPI), C, OCaml, Crystal

## Compiler — [`compiler`](https://github.com/zane-lang/compiler)

- [x] **Front end**
  - [x] Parsing to a concrete syntax tree (CST), with a machine-checked proof
    that the grammar is unambiguous
  - [x] Desugaring (SST)
  - [x] Name resolution and type checking (TST)
- [x] **Back end**
  - [x] Code generation through LLVM, linking with a bundled C runtime
  - [x] Linux, macOS and Windows, built from any of them
  - [x] Compile-time evaluation in optimized builds, memoization, tiered builds
  - [x] Separate compilation: one object per package, prebuilt dependencies
- [x] **Calling C** — a package's C code, compiled and checked by the compiler
- [x] **Released toolchains** for Linux x86-64, macOS and Windows x86-64
- [~] **Diagnostics & error reporting**

## The `zane` command — [`zane`](https://github.com/zane-lang/zane)

- [x] Projects: `init`, `check`, `build`, `run`, `test`, `clean`
- [x] Dependencies: `add`, `remove`, `update`, `dev`, `remap`, `fetch`, `tree`, the package cache
- [x] Toolchains: `toolchain install`, `toolchain update`, `self update`
- [x] Inspecting the compiler's view of a program: `inspect`
- [x] Released binaries and installers for Linux, macOS and Windows
- [ ] Publishing packages: `release` and `release upload`

## Standard packages

Packages provided by Zane itself.

- [x] `core` — basic types, text, containers, control flow, console — [`core`](https://github.com/zane-lang/core)
- [x] `math` — math functions over `core`'s numbers — [`core`](https://github.com/zane-lang/core)
- [ ] `std` — the standard library

## Tooling & ecosystem

- [~] **Editor & language support**
  - [x] Tree-sitter grammar for Zane, generated from the compiler's grammar
  - [x] Neovim plugin — [`zane-nvim`](https://github.com/zane-lang/zane-nvim)
  - [x] Typst syntax highlighting, generated from the compiler's grammar
  - [x] Tree-sitter grammar for Coda — [`tree-sitter-coda`](https://github.com/zane-lang/tree-sitter-coda)
  - [ ] Language server (LSP)
- [~] **Documentation**
  - [x] Reference: the [specification](https://github.com/zane-lang/spec)
  - [ ] A beginner's guide or tutorial
- [x] **Project presence**
  - [x] Brand & logos — [`logos`](https://github.com/zane-lang/logos)
  - [x] Organization profile & community health files — [`.github`](https://github.com/zane-lang/.github)
  - [-] Website — [`website`](https://github.com/zane-lang/website)
  - [-] Documentation site — [`docs`](https://github.com/zane-lang/docs)
- [-] **`checkpoint`** — a shell-history rollback utility — [`checkpoint`](https://github.com/zane-lang/checkpoint)

## Contributing

Interested in helping move an item forward? See
[CONTRIBUTING.md](CONTRIBUTING.md) and pick up an issue on the relevant
repository.
