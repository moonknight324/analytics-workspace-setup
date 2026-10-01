# Team GitHub Workflow

## Branching Strategy
- `main` holds releasable code only. Nobody commits directly to it.
- Work happens on feature branches named `[type]/[short-description]`, where type is one of `feature`, `fix`, `docs`, `refactor` or `chore`. Example: `feature/data-ingestion`.
- Branches are deleted after merge.

## Commit Message Convention
- Format: `[type]: [description]`, with an optional body explaining why.
- Types used: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`.
- Why: it enables automated changelog generation and gives a clear, searchable history.

## Pull Request Review Process
- Every PR needs at least one approval before merge.
- Reviews focus on correctness, clarity, data integrity and test coverage.
- Commit messages are reviewed as part of code review.
- PR descriptions must link the related issue (for example `Closes #1`).

## GitHub Issue Tracking
- Every feature or fix starts with an issue.
- Issues have a descriptive title, a description of why the work matters and what done means, at least one label, and an assignee.
- Issues are closed automatically when the corresponding PR is merged.
