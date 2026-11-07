# Contributing

This repository documents a completed Software Engineering course project (AIUB, Summer 25-26, Group 03). It is **not open to outside code contributions** — there is no running application in this repository yet, and the academic submission is finished. This file records the conventions the team used during development and the conventions used for documentation updates after the course ended, so the repository's own history stays consistent.

## Who this applies to

- **Team members** (Ishmam Mubtasim, Tanmay Roy Rony, Afroza Akter Neha, Sanjida Affrin Bristi, Sudipto Karmaker Bipro) making documentation corrections or adding the source code later.
- **Anyone else:** please open an [issue](../../issues/new/choose) instead of a pull request if you spot an error (broken link, factual mistake, typo). Issues are welcome; code or content pull requests from outside the team will not be merged, since this is a graded academic submission.

## Branching

| Branch | Purpose |
|---|---|
| `main` | Stable branch. Default branch. Protected — no direct pushes. |
| `dev` | Integration branch for merged work. |
| `stage` | Pre-release branch used for release candidates. |
| `feature/<short-name>` or `docs/<short-name>` | Short-lived branch for one task or one documentation change. Deleted after merge. |

All changes go through a branch and a pull request — never a direct push to `main`.

## Commit messages

Commits follow a `type: description` format, with a Trello task ID in parentheses where one applies:

```text
feat: implement user login page (T-46)
fix: validate numeric input for orphanage Max Capacity (TC_4)
docs: add requirements summary
test: add validation test case for orphanage capacity
chore: update .gitignore for Visual Studio files
release: promote stage to main (v1.1.0)
```

Use the imperative mood ("add", not "added" or "adding"), keep the summary line under ~72 characters, and keep each commit to one logical change rather than bundling unrelated edits.

**Types used in this project:** `feat`, `fix`, `docs`, `test`, `chore`, `release`. Use `refactor` once source code exists and a change restructures it without changing behavior.

## Pull requests

- Open a pull request into `dev` (or into `main` only for a release promotion, as the two historical release PRs #58 and #59 did).
- Fill in the [pull request template](.github/pull_request_template.md) — in particular, confirm no passwords, connection strings, or real child/personal data are included.
- Reference the related Trello task ID in the PR title, e.g. `feat: implement user login page (T-46)`.
- At least one other team member should review before merging, where practical.

## Reporting a documentation issue

Use the [issue templates](.github/ISSUE_TEMPLATE/) to report a broken link, a factual error, or a gap in the documentation. Please do not include any real child data, student IDs, or credentials in an issue — see the [security notes](docs/project-management/README.md) for what this repository treats as sensitive.
