# pipeline-drill

A small, live example repository used in our team workshop on how we handle pull requests on GitHub.

## What this repo demonstrates

- **Feature branches:** small, focused changes developed on a branch (for example `feature/usage-notes`) instead of directly on `main`.
- **Draft pull requests:** open the PR early as a draft while the work is in progress, then mark it ready for review when it is done.
- **Continuous integration:** every push and every pull request runs a GitHub Actions workflow (`.github/workflows/ci.yml`) that builds a small artifact named `build-output`.
- **Review etiquette:** reviews are left as comments, approvals, or change requests, with inline notes attached to specific lines.
- **Keeping the branch current:** the default branch moves on while a PR is open, so the PR branch is synced with `main` before the review finishes.

## Usage

- Create a feature branch such as `feature/usage-notes` for every change.
- Open a **draft** pull request as soon as the work starts, and mark it ready for review once it is finished.
- Wait for the `CI` workflow to finish and check that the `build-output` artifact was uploaded.
- Keep the branch up to date by updating it from `main` whenever the default branch moves ahead.
- Merge only after the checks pass and the review is complete.

## Support

Questions or feedback about this workshop example? Open an issue or leave a comment on the relevant pull request.

## Layout

| Path | Purpose |
| --- | --- |
| `README.md` | This document: what the repository is and how we use it. |
| `.github/workflows/ci.yml` | The CI pipeline that runs on pushes and pull requests and uploads the `build-output` artifact. |
