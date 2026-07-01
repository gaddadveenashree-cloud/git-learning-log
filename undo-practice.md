```markdown
# Git Toolkit

This file documents the Git undo and recovery tools I've learned.
```
git add undo-practice.md stages the file, telling Git you want to include it in the next commit.
git commit -m "Add undo-practice.md" saves a snapshot of the staged changes with a descriptive message"
git push uploads your new commit to GitHub so it is backed up remotely.

```markdown

## Reset

- git reset --soft HEAD~1: undo last commit, keep changes staged
- git reset --mixed HEAD~1: undo last commit, keep changes in working directory (default)
- git reset --hard HEAD~1: undo last commit and discard all changes (dangerous!)
- Only use reset on commits that haven't been pushed
```
```markdown

## Revert

- git revert HEAD: create a new commit that undoes the last commit
- git revert is safe for shared/pushed branches because it doesn't rewrite history
- The original commit stays in the log, plus a new "undo" commit is added
```