## Git concepts

1. `git merge branch-name`
- git merge will merge the changes of two branches. It preserves the branch diversion history and creates a special *merge commit*, which has the snapshot of the project with both merged branches changes.
- Even If there are no merge conflicts, the special merge commit is created to merge the branches.
- When we merge feature branch with main branch with no new commits, git won't create merge commit. The pointer is moved to feature branch.
> merging two branches flow
you are on feature branch
- git pull origin main
Resolve If there are any conflicts, then you can push feature branch to remote and create PR against main.

2. `git rebase branch-name`
- git rebase command will reapply your local feature-branch changes on top of latest remote main branch, one by one.
- rebase will rewrite the history
- if conflicts occur during rebase, we resolve them and add to staging area and continue with rebase.
> rebase two branches flow
you are on feature branch
- git fetch origin main-branch
- git rebase origin/main-branch
- If conflicts occur, resolve them and push feature branch to remote and create PR against main