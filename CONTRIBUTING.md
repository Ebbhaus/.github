# How we ship code at Ebbhaus

This is the default engineering workflow for all Ebbhaus repos. Individual
repos can override it with their own `CONTRIBUTING.md` when they need to.

## Branching

- `main` is always deployable.
- Work happens on short-lived branches off of `main`.
- Name branches `<yourhandle>/<short-description>` or `<type>/<description>`
  where type is `feat`, `fix`, `chore`, `infra`, etc.
- Delete branches after merge. Don't leave stale branches lying around.

## Commits

- Write commits that explain *why* the change is needed, not just what changed.
- Small, focused commits are easier to review and revert.
- We use Conventional Commits (`feat:`, `fix:`, `chore:`, etc.) so release
  automation and changelogs can parse them.

## Pull requests

- Every change goes through a PR. No direct pushes to `main`.
- Fill out the PR template — especially the test plan. If there's nothing to
  test, say so and why.
- Keep PRs under ~400 lines of diff when you can. Split larger work.
- CI must be green before merge.
- At least one approval from a codeowner is required.
- Default merge strategy is **Squash and merge**.

## Code review

- Review within one business day when you're tagged. If you can't, say so and
  reassign.
- Reviewers: focus on correctness, clarity, and whether the change matches the
  stated goal. Style nits are fine but mark them as nits.
- Authors: don't take feedback personally, and don't argue — either apply it,
  push back with reasoning, or add a TODO and move on.

## Testing

- New behavior needs tests. Regressions get a test that would have caught it.
- Don't disable or skip tests without an issue link explaining why.
- Prefer fast, deterministic tests. Flaky tests are bugs.

## Secrets and credentials

- Never commit secrets. If you do, rotate them immediately and tell
  #eng-security.
- Use the repo or environment secrets in GitHub Actions, never hardcode.
- Production credentials live in our secrets manager, not in repos.

## Questions

Ask in `#engineering` on Slack. For security-sensitive things, see
[`SECURITY.md`](./SECURITY.md).
