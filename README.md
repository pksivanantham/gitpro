
# This is updated from new repo


`git fetch
git rebase origin/master`
In a nutshell:

`git merge branchname` takes new commits from the branch branchname, and adds them to the current branch.
If necessary, it automatically adds a "Merge" commit on top.

`git rebase branchname` takes new commits from the branch branchname, and inserts them "under" your changes. More precisely, it modifies the history of the current branch such that it is based on the top of branchname, with any changes you made on top of that.

`git pull` is basically the same as` git fetch; git merge origin/master`.

`git pull --rebase` is basically the same as `git fetch; git rebase origin/master`.


So why would you want to use `git pull --rebase` rather than git pull? Here's a simple example:

You start working on a new feature.

By the time you're ready to push your changes, several commits have been pushed by other developers.

If you `git pull` (which uses merge), your changes will be buried by the new commits, in addition to an automatically-created merge commit.

If you `git pull --rebase` instead, git will fast forward your master to upstream's, then apply your changes on top.

`git pull --allow-unrelated-histories` Scenario 1:
1. Created repo in local and added commits
2. Created repo in github with readme file.


Now we want local repo to sync with origin repository then we have to use pull with --allow-unrelated-histories `git pull --allow-unrelated-histories`

