# Contributing to the Manuscript

Thank you for contributing to this manuscript! This document outlines our workflow for collaborative manuscript writing.

## Maintainer and Contributors

- **Maintainer**: @bonschorno
- **Contributors**: @seawaR, @larnsce

## Setup

This project uses `renv` for R package management. After cloning the repository:

```r
renv::restore()
```

This will install all required packages as specified in the lockfile.

## Workflow

### 1. Track TODOs as Issues

We use GitHub Issues to track all manuscript tasks, including:

- Sections to write or revise
- Figures and tables to create
- References to add
- Analyses to run
- Review comments to address

Create a new issue for each task with a descriptive title and any relevant details.

### 2. Work on Issues via Pull Requests

When working on an issue:

1. Switch to the `dev` branch and ensure it's up to date:
   ```bash
   git checkout dev
   git pull origin dev
   ```

2. Make your changes to the manuscript or related files

3. Commit your changes with clear commit messages:
   ```bash
   git add .
   git commit -m "Address #<issue-number>: Brief description"
   ```

4. Push to `dev` and open a Pull Request from `dev` to `main`:
   ```bash
   git push origin dev
   ```

5. In the PR description, reference the issue (e.g., "Closes #<issue-number>")

6. Request review from the maintainer or other contributors

### 3. Review Process

- All PRs require review before merging to `main`
- The maintainer (@bonschorno) has final approval
- Address review comments by pushing additional commits to `dev`

### 4. Merging to Main

- Only the maintainer merges from `dev` to `main`
- `main` represents the current "official" version of the manuscript
- Major milestones (e.g., submission versions) are tagged on `main`

## Best Practices

- Keep PRs focused on specific issues
- Write clear commit messages
- Update issue comments with progress or blockers
- Render the manuscript locally before opening a PR to check for errors
- Use Quarto's visual editor or preview features to verify formatting
- If you add new R packages, run `renv::snapshot()` to update the lockfile and commit the changes

## Questions?

Contact @bonschorno if you have questions about the workflow.
