* Check the log with `git log --online`
  Count the lines with `git rev-list --count HEAD`: 29 total commits
  The commits were made in `graph.md`,`README.md`,`shell.md`,etc.
* Automically generated commit messages from Github: *Enhace graph.md with predictions and result, Add initial content to graph.md, etc.*
* the email shown is the actual e-mail. Step 1 can mask the private e-mail but can not change the history to mask the private e-mail if the private e-mail was used to create the commits before masking.
* most changed file: `labs/01/dataset.md` (11 times)
1. `git status`:
> On branch main  
> Your branch is up to date with 'origin/main'.  
> nothing to commit, working tree clean  

2. `cp "C:\Users\daoth\Pictures\Screenshots\git-graph.png" labs/03/`: copy file onto labs 03  
3. `git status`:
> On branch main
> Your branch is up to date with 'origin/main'.
> Untracked files:  
>  (use "git add <file>..." to include in what will be committed)  
>        labs/03/git-graph.png
> nothing added to commit but untracked files present (use "git add" to track)
4. `git add labs/03`: Stage the file
5. `git status`:
> On branch main
> Your branch is up to date with 'origin/main'.
> Changes to be committed:
> (use "git restore --staged <file>..." to unstage)
> new file:   labs/03/git-graph.png
6. `git commit -m "Add git-graph.png"` :
> [main e493407] Add git-graph.png
> 1 file changed, 0 insertions(+), 0 deletions(-)
> create mode 100644 labs/03/git-graph.png
7. `git status`:
> On branch main
> Your branch is ahead of 'origin/main' by 1 commit.
> (use "git push" to publish your local commits)
> nothing to commit, working tree clean
8. `git push`:
> Enumerating objects: 9, done.
> Counting objects: 100% (9/9), done
> Delta compression using up to 8 threads
> Compressing objects: 100% (6/6), done.
> Writing objects: 100% (6/6), 184.52 KiB | 26.36 MiB/s, done.
> Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
> remote: Resolving deltas: 100% (2/2), completed with 1 local object.
> To https://github.com/thdao6/data-integration-labs.git 
> e425b35..93fbd10  main -> main







