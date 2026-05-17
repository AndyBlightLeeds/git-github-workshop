# Git Commands for the workshop

| Command | Explanation |
| --- | --- |
| `git branch` | Lists the branches in the current repo. |
| `git branch <branch>` | Creates a new branch but does not switch to it. |
| `git branch  -a` | Lists the branches in the current and any remote repos. |
| `git branch -m <new branch name>` | Modifies the name of the current branch to `<new branch name>` |
| `git branch -d <branch name>` | Deletes the specified branch name. |
| `git checkout -b <branch>` | Creates a new branch and switches to it. |
| `git checkout <branch>` | Switches to the specified branch. |
| `git commit` | Commit all staged files to the Git repo. An editor is opened up so you can write a message.  Great for longer messages. |
| `git commit -m "Commit message"` | Commit all staged files to the Git repo using the given commit message. |
| `git commit -am "Commit message"` | Commit all modified files that Git knows about to the Git repo using the given commit message. Great for short messages. |
| `git commit --amend` | Amend the current revision.  Files can be added using `git add`, any modified files are included and the commit message can be edited. Great for short messages. |
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
| `git tag <tag name>` | Creates a tag using \<tag name> and associates it with the current revision.  |

## Other commands

| Command | Explanation |
| --- | --- |
| `cat .git/config` | Displays the contents of the `.git/config` file. |
| `ls .git` | Lists the contents of the `.git` directory. |
