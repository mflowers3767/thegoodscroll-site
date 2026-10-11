# Contributing

## Source of truth

This GitHub repository and its default branch `master` are the authoritative source for this product. Local folders, dated agent workspaces, and deployed server files are not substitutes for committed Git history.

## Required workflow

1. Work only in a clone or worktree of this canonical repository.
2. Before changing files, run `git status`. If the tree is not clean, stop and preserve or reconcile the existing work; never overwrite it.
3. Run `git fetch --prune origin`, switch to `master`, and update it with `git pull --ff-only origin master`.
4. Check open issues, branches, and pull requests for overlapping work.
5. Create one task branch from updated `master`: `codex/<issue>-<slug>` or `claude/<issue>-<slug>`.
6. Make the scoped change and run the relevant tests or build.
7. Commit and push the task branch to GitHub before any deployment.
8. Open a pull request to `master`. Merge only after the diff and checks are reviewed.
9. Update local `master` before starting the next task.

## Collaboration

Only one agent may change the same portion of the product at a time. Work on separate areas still uses separate branches and pull requests so every change remains reviewable and current.

## Deployments

Do not deploy uncommitted or unpushed code. A necessary emergency server edit must be captured immediately in a branch and pull request, then verified against the deployed result. Record the deployed commit SHA when practical.

## Security and generated artifacts

Never commit credentials, tokens, passwords, `.env` files, private configuration, database dumps, production exports, customer data, or generated diagnostics unless a repository-specific rule explicitly identifies a sanitized artifact as safe.
