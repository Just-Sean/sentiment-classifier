# Contributing

How we work on this repo. Every change goes through a branch and a pull request (PR), and the other person reviews and merges it. Nobody merges their own PR into `main`.

## The workflow

1. **Open an issue** for the change, one per function (or test, or doc). Put it on the project board. The board holds code work only; planning stays off it.
2. **Make a branch** off an up-to-date `main`:

   ```bash
   git checkout main
   git pull
   git checkout -b feature/drop-three-star-reviews
   ```

3. **Write the code and its test.** Run `pytest` before you push.
4. **Push and open a PR** into `main`. Link the issue in the description (see below).
5. **The other person reviews it.** They ask for changes or approve.
6. **The reviewer merges it** once it's approved. The issue closes on its own.

## Branch names

Use `<type>/<description>`, lowercase, with hyphens:

| Type | Use it for | Example |
| --- | --- | --- |
| `feature/` | New code | `feature/count-cleaning-issues` |
| `fix/` | A bug fix | `fix/html-entity-decoding` |
| `test/` | Tests only | `test/add-label-tests` |
| `docs/` | README, this file, and other docs | `docs/update-readme` |

## Linking issues

- **`Closes #12`** in the PR description closes issue 12 when the PR merges into `main`. GitHub also accepts `Fixes` and `Resolves` ([GitHub docs](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue)).
- **One keyword per issue:** `Closes #4, closes #7`.
- **Keywords only work on PRs into `main`.** On a PR into any other branch, GitHub ignores them.
- **`Part of #12`** links a PR to an issue without closing it. Use it when a PR finishes only part of the issue.

## Commit messages

Start with a type, then say what changed ([Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)):

```
feat: add drop_three_star_reviews
test: check that 3-star reviews raise an error in label_sentiment
fix: decode HTML entities before stripping tags
docs: add run instructions to README
```

When we pair on a commit, add a co-author line after a blank line, so GitHub credits both of us ([GitHub docs](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors)):

```
feat: add load_reviews

Co-authored-by: Name <github-email-or-noreply-address>
```

## What the reviewer checks

- [ ] `pytest` passes.
- [ ] Each function does one job, and its name says what the job is.
- [ ] The script starts with a short note on what it does and how to run it.
- [ ] Paths come in as arguments, not hard-coded.
- [ ] No data files in the PR (`data/` is git-ignored; keep it that way).

## Never commit

- Data files (`.jsonl`, `.jsonl.gz`, `.parquet`, `.csv`). GitHub blocks files over 100 MiB.
- Model checkpoints or the Hugging Face cache (`.cache/`).
