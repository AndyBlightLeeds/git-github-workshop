# Git Commands for the workshop

## Using Git on your own

| Command | Explanation |
| --- | --- |
| `ls .git` | Lists the contents of the `.git` directory. |
| `cat .git/config` | Displays the contents of the `.git/config` file. |
| `git status` | Displays the status of the git repository. |
| `git log` | Displays details about the commits on this bran in the repo. |
| `git add <file>` | Add the `file` to the staged area of the repo. |
| `git commit` | Opens an editor so you can add a message.  When the editor exits and a message has been saved, the commit happen. |
| `git commit -m "<message>"` | When enter is pressed, any staged changes are committed with the `<message>`. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the `<message>`. |
| `git commit --amend` | Opens an editor so you can modify the last commit. |

## Branches Practical

| Command | Explanation |
| --- | --- |
| `git branch` | Lists the branches in the current repo. |
| `git branch  -a` | Lists the branches in the current and any remote repos. |
| `git branch -m <new branch name>` | Modifies the name of the current branch to `<new branch name>` |
| `git branch -d <branch name>` | Deletes the specified branch name. |
| `git checkout -b <branch>` | Creates a new branch and switches to it. |
| `git checkout <branch>` | Switches to the specified branch. |
| `git diff <branch>` | Show the differences between this branch and the specified `<branch>` |
| `git difftool <branch>` | Show the differences between this branch and the specified `<branch>` in an external program, e.g. `meld` |
| `git merge <branch>` | Merges the specified branch into the current branch. |
| `git mergetool <branch>` | Perform the merge in a different program, e.g. `meld`. Great when things go wrong with the automatic merge. |
| `git push` | Pushes any changes on your current branch to the server. |
| `git push --set-upstream origin <your_branch>` | Add a copy of the local branch to the server and push any changes on your local branch to the server. |
| `git switch -c <branch>` | Creates a new branch and switches to it. |
| `git switch <branch>` | Switches to the specified branch. |

## Practicals

| Command | Explanation |
| --- | --- |
| `git branch` | Lists the branches in the current repo. |
| `git branch <branch>` | Creates a new branch but does not switch to it. |
| `git branch  -a` | Lists the branches in the current and any remote repos. |
| `git branch -m <new branch name>` | Modifies the name of the current branch to `<new branch name>` |
| `git branch -d <branch name>` | Deletes the specified branch name. |
| `git checkout -b <branch>` | Creates a new branch and switches to it. |
| `git checkout <branch>` | Switches to the specified branch. |
| `git commit -am "Commit message"` | Commit the current changeset to the Git repo. |
| `git commit --amend` | Amend the current revision.  Files can be added using `git add`, any modified files are included and the commit message can be edited. |
| `git diff <branch>` | Show the differences between this branch and the specified `<branch>` |
| `git difftool <branch>` | Show the differences between this branch and the specified `<branch>` in an external program, e.g. `meld` |
| `git fetch` | Fetches any changes from the default upstream repo (normally `origin`). |
| `git log` | Shows the revisions on the current branch of the repo. |
| `git merge <branch>` | Merges the specified branch into the current branch. |
| `git mergetool <branch>` | Perform the merge in a different program, e.g. `meld`. Great when things go wrong with the automatic merge. |
| `git pull` | Pulls any changes from the server and merges the changes into your local branch.|
| `git push` | Pushes changes on your local branch to the server. |
| `git push --set-upstream origin <your_branch>` | Pushes your local branch to the server. |
| `git status` | Shows the status of the repo. |
| `git switch -c <branch>` | Creates a new branch and switches to it. |
| `git switch <branch>` | Switches to the specified branch. |
