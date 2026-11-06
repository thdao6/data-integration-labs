Round 1  
* Prediction: The main branch starts with the commit "Download the data", then a new branch would be created named `clean`. The next 2 commits happen in the branch. `git checkout master` returns to the main branch and `git merge clean` merges the branch.
* Results: The branch `clean` path doesn't deviate deviate from `master` since there were no new commits in `master`. The timeline moves in a straight line.
  `git merge clean` does not make a new commit, but moves `master` to the standpoint of `clean`.

Round 2
* Prediction: `git checkout -b plot` creates a new branch named `plot`. The commmit "PLot cyclists per month" would be commited in the branch `plot`. `git checkout master` returns to the main branch `master`. The commit "Describe the data in the README" would be commited in the main branch. `git merge plot` merges the main branch `master` with `plot`.
* Results: The main branch split into 2 since the 2 commits were commited in different branches. `git merge plot` has two parents `Describe the data in the README` and `Plot cyclists per month`. This merge was not a fast forward merge since there were 2 commits commited in different branches before being merged. The tag `v1.0` marks the current version of the main branch.

Round 3

