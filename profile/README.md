<!-- markdownlint-disable-next-line MD041 -- logo floats before the H1 by design -->
<img height="96" align="right" src="https://raw.githubusercontent.com/zane-lang/logos/main/zane/zane.svg" alt="Zane logo" />

# Zane

**Zane** is a systems programming language built around a simple idea: the
compiler should keep the intent you wrote down, and turn strictness into
performance instead of ceremony. It gives you deterministic,
garbage‑collection‑free memory management without giving up safety.

---

## The ecosystem

| Repository | What it is |
| --- | --- |
| [**spec**](https://github.com/zane-lang/spec) | The language specification and its design stories. |
| [**compiler**](https://github.com/zane-lang/compiler) | The Zane compiler and command‑line interface. |
| [**coda**](https://github.com/zane-lang/coda) | The Coda configuration format for Zane — a compact, readable alternative to JSON. |
| [**tree-sitter-coda**](https://github.com/zane-lang/tree-sitter-coda) | A Tree‑sitter grammar for Coda. |
| [**website**](https://github.com/zane-lang/website) | The Zane website. |
| [**docs**](https://github.com/zane-lang/docs) | Documentation for the language and tooling. |
| [**logos**](https://github.com/zane-lang/logos) | The official Zane logos and brand assets. |

---

## Getting started

The compiler is developed inside a reproducible [devbox](https://www.jetify.com/devbox)
environment. To build it from source:

```sh
# Install devbox (once)
curl -fsSL https://get.jetify.com/devbox | bash

# Clone and build
git clone https://github.com/zane-lang/compiler
cd compiler
devbox shell
just init   # submodules, vcpkg dependencies, and meson
just build
```

Run `just` inside the dev shell to see every available command.

---

## Get involved

Zane is an open project and contributions are welcome — issues, pull requests,
and discussion all help. Start with the [contributing guide](https://github.com/zane-lang/.github/blob/main/CONTRIBUTING.md)
and the [code of conduct](https://github.com/zane-lang/.github/blob/main/CODE_OF_CONDUCT.md),
then pick a repository above and dive in.
