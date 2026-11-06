Round 1  
* Prediction: The main branch starts with the commit "Download the data", then a new branch would be created named `clean`. The next 2 commits happen in the branch. `git checkout master` returns to the main branch and `git merge clean` merges the branch.
* Results: The branch `clean` path doesn't deviate deviate from `master` since there were no new commits in `master`. The timeline moves in a straight line.
  `git merge clean` does not make a new commit, but moves `master` to the standpoint of `clean`.

Round 2
* Prediction: `git checkout -b plot` creates a new branch named `plot`. The commmit "PLot cyclists per month" would be commited in the branch `plot`. `git checkout master` returns to the main branch `master`. The commit "Describe the data in the README" would be commited in the main branch. `git merge plot` merges the main branch `master` with `plot`.
* Results: The main branch split into 2 since the 2 commits were commited in different branches. `git merge plot` has two parents `Describe the data in the README` and `Plot cyclists per month`. This merge was not a fast forward merge since there were 2 commits commited in different branches before being merged. The tag `v1.0` marks the current version of the main branch.

Round 3
* Prediction: `git commit -m "Delete outliers"` creates a commit directly in the main branch. `git revert HEAD` / `git reset HEAD 2` ??
* Results:  `git commit -m "Delete outliers"` creates a commit directly in the main branch. `git revert HEAD` creates a new commit the revert the previous commit, thus recording itself in the branch. `git reset HEAD~2` deletes the commits in the branch itself, rewriting the timeline. Commits with no branch attached are in a detached head state and can be reached using reflog. For reverting bad commits one should use `git revert HEAD`, since `git reset HEAD` rewrites the branch whole history.  

Round 4
* Prediction: `git checkout v1.0~1` returns to branch where v1.0 was tagged?
* Results: `git checkout v1.0~1` returns the HEAD to the commit before `git tag v1.0`. The commit "Try a log scale" is then created in a detached head state and was not reachable after `git checkout master`, `reflog` makes the commit reachable.
