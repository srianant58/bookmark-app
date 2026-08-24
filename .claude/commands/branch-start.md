---
description: Create and switch to a new git branch, synced with the latest main
argument-hint: <branch-name>
allowed-tools: Bash(git:*)
---

Create a new git branch off the latest `main` and switch to it.

Branch name: $ARGUMENTS

Steps to follow:
1. Run `git status` to check for uncommitted changes. If there are any, stop and warn the user instead of proceeding — don't discard their work.
2. Run `git checkout main` then `git pull origin main` to sync local main with the remote.
3. If `$ARGUMENTS` is empty, ask the user for a branch name instead of guessing. Otherwise run `git checkout -b $ARGUMENTS` to create and switch to the new branch.
4. Confirm the branch was created with `git branch --show-current` and report the result to the user.

Do not make any code changes as part of this command — its only job is preparing the branch.
