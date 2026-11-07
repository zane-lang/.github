<!-- markdownlint-disable-next-line MD041 -- logo floats before the H1 by design -->
<img height="96" align="right" src="https://raw.githubusercontent.com/zane-lang/logos/main/zane/zane.svg" alt="Zane logo" />

# Zane

**Zane** is a systems programming language built around a simple idea: the
compiler should keep the intent you wrote down, and turn strictness into
performance instead of ceremony. It gives you deterministic memory management
with no garbage collector and no lifetime annotations, without giving up
safety.

```zane
package hello;

import core$;

Unit main() {
	console Console(@program$console);
	console!print("Hello, Zane!");
	return Unit();
}
```

Zane is young and changes quickly. Its compiler works and is released, but
there is no tutorial yet: the [specification](https://github.com/zane-lang/spec)
is the reference.

## Start here

1. **Try it**: install the [`zane`](https://github.com/zane-lang/zane) command
   and follow its first-project steps.
2. **Learn the ideas**: read the spec's
   [`foundations.md`](https://github.com/zane-lang/spec/blob/main/spec/foundations.md),
   then the reading order in the [spec README](https://github.com/zane-lang/spec#where-to-start).
3. **See real code**: the [`core` package](https://github.com/zane-lang/core)
   and its tests are written in Zane.

## Design philosophy

Zane gives inherited language design no special authority. **Existing languages are things to investigate, not templates to follow.** Every feature and restriction is expected to earn its place from first principles rather than from convention.

That also means making deliberately strong claims. Strong claims are easy to falsify; when one breaks, the counterexample exposes a requirement the design was missing. Zane's own decisions are subject to the same treatment — nothing is preserved merely because we already designed it that way.

The longer reasoning, including the bets that survived and the ones that did not, lives in the [specification's design stories](https://github.com/zane-lang/spec/tree/main/stories).

## Repositories

| Repository | What it is |
| --- | --- |
| [**zane**](https://github.com/zane-lang/zane) | The `zane` command: create, build, run and test projects. Start here. |
| [**spec**](https://github.com/zane-lang/spec) | The language specification and its design stories. |
| [**compiler**](https://github.com/zane-lang/compiler) | `zanec`, the compiler that `zane` runs. |
| [**core**](https://github.com/zane-lang/core) | The `core` and `math` packages: numbers, text, lists and control flow. |
| [**zane-nvim**](https://github.com/zane-lang/zane-nvim) | Neovim support for Zane. |
| [**coda**](https://github.com/zane-lang/coda) | Coda, the configuration format of Zane's project files. |
| [**tree-sitter-coda**](https://github.com/zane-lang/tree-sitter-coda) | A Tree‑sitter grammar for Coda. |
| [**logos**](https://github.com/zane-lang/logos) | The Zane and Coda logos. |

The `website`, `docs`, `template`, `test-package`, `checkpoint` and
`coderabbit` repositories are not needed to learn or use Zane right now.

## Get involved

Zane is an open project and contributions are welcome — issues, pull requests,
and discussion all help. Start with the [contributing guide](https://github.com/zane-lang/.github/blob/main/CONTRIBUTING.md)
and the [code of conduct](https://github.com/zane-lang/.github/blob/main/CODE_OF_CONDUCT.md),
then pick a repository above and dive in.
