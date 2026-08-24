---
description: Commit current changes and push the branch to GitHub
argument-hint: <commit message>
allowed-tools: Bash(git:*)
---

Commit the current working-tree changes and push the current branch to GitHub. Do NOT merge into main and do NOT delete any branch — the user handles merging (via GitHub) and branch cleanup themselves.

Commit message: $ARGUMENTS

Steps to follow:
1. Run `git status` to see what changed. If there's nothing to commit, tell the user and stop.
2. Run `git branch --show-current`. If it's `main`, stop and warn the user — this command is only for feature branches and must never commit/push directly to main.
3. Run `git add .`, then review what got staged (`git status`) — flag anything that looks like it shouldn't be committed (secrets, build artifacts, etc.) before proceeding.
4. If `$ARGUMENTS` is empty, ask the user for a commit message instead of guessing one. Otherwise commit with that message.
5. Push the branch to origin with `git push -u origin <current-branch-name>`.
6. Report the pushed branch name and remind the user that merging into `main` on GitHub and any branch cleanup is up to them.
