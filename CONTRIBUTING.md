# Contributing to Zane

Thanks for your interest in contributing to [Zane](https://github.com/zane-lang)!
This guide applies across every repository in the organization. Individual
repositories may add their own `CONTRIBUTING.md` or `CLAUDE.md` with
project‑specific details — read those too when they exist.

## Code of conduct

Participation in Zane is governed by our
[Code of Conduct](CODE_OF_CONDUCT.md). By taking part, you agree to uphold it.

## Ways to contribute

- **Report bugs.** Open an issue using the bug report template on the relevant
  repository.
- **Request features.** Open an issue using the feature request template.
- **Improve docs.** Corrections and clarifications to the
  [spec](https://github.com/zane-lang/spec),
  [docs](https://github.com/zane-lang/docs), or any README are always welcome.
- **Write code.** Fix a bug, implement a feature, or improve tooling.

If you're planning a large or design‑changing contribution, open an issue to
discuss it first — it saves everyone time.

## Development setup

Most Zane repositories are built inside a reproducible
[devbox](https://www.jetify.com/devbox) environment and expose their tasks
through a [`justfile`](https://github.com/casey/just). A typical flow:

```sh
# Install devbox once
curl -fsSL https://get.jetify.com/devbox | bash

# In a cloned repository
devbox shell     # enter the toolchain environment
just             # list the available recipes
just init        # bootstrap submodules / dependencies, where applicable
just build       # build
just test        # run the tests
```

Always prefer the `just` recipes over hand‑running toolchain commands — they
encode the exact flags and environment each project expects. Check the repo's
`justfile` first.

## Pull requests

1. **Fork and branch.** Create a topic branch off `main` with a descriptive
   name.
2. **Keep it focused.** One logical change per pull request. Small, reviewable
   PRs are merged faster.
3. **Build and test locally** before pushing (`just build`, `just test`).
4. **Write clear commits.** Explain *why*, not just *what*. Use the present
   tense (e.g. "Add arena reset").
5. **Fill in the PR template.** Describe the change, link related issues, and
   note anything reviewers should focus on.
6. **Be responsive to review.** Reviews (including automated ones from
   CodeRabbit) are part of the process — address feedback or explain why a
   suggestion doesn't apply.

## Reporting security issues

Please **do not** open public issues for security vulnerabilities. Follow the
process in [SECURITY.md](SECURITY.md) instead.

## Questions

See [SUPPORT.md](SUPPORT.md) for where to ask questions and get help.
