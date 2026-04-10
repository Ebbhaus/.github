# Contributing

Thanks for contributing to Ebbhaus. These are the default guidelines that apply
across all repositories in the org. Individual repos may override them with
their own `CONTRIBUTING.md`.

## Getting started

1. Clone the repo and install dependencies as described in its README.
2. Create a branch off of `main` for your work.
3. Make your changes in small, focused commits.
4. Open a pull request against `main` when ready.

## Branches

Use descriptive branch names prefixed by type, e.g.:

- `feat/<short-description>`
- `fix/<short-description>`
- `chore/<short-description>`
- `docs/<short-description>`

## Commits

We loosely follow [Conventional Commits](https://www.conventionalcommits.org/).
A good commit message explains the *why* more than the *what*:

```
feat(api): add retry with exponential backoff to ingestion client

The ingestion endpoint occasionally returns 503 during deploys. Retrying
with backoff avoids spurious failures in the learner pipeline.
```

## Pull requests

- Keep PRs small and reviewable. Split large changes when you can.
- Fill out the PR template, including the test plan.
- Make sure CI is green before requesting review.
- At least one approving review is required before merging.
- Prefer "Squash and merge" unless the repo says otherwise.

## Code style

- Follow whatever linter/formatter the repo ships with (Prettier, Ruff, gofmt,
  etc.). Don't hand-format around the tool.
- Write tests for new behavior and regressions you fix.
- Don't leave dead code, commented-out blocks, or TODOs without context.

## Reporting security issues

Please **do not** open public issues for security problems. See
[`SECURITY.md`](./SECURITY.md) for how to report them.
