## Git concepts

1. `git merge branch-name`
- git merge will merge the changes of two branches. It preserves the branch diversion history and creates a special *merge commit*, which has the snapshot of the project with both merged branches changes.
- Even If there are no merge conflicts, the special merge commit is created to merge the branches.
- When we merge feature branch with main branch with no new commits, git won't create merge commit. The pointer is moved to feature branch.
> merging two branches flow
you are on feature branch
- git pull origin main
Resolve If there are any conflicts, then you can push feature branch to remote and create PR against main.

