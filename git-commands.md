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
| `git commit -m "<message>"` | When enter is pressed, any staged changes are committed with the <message>. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the <message>. |
| `git commit --amend` | Opens an editor so you can modify the last commit. |

## Branches Practical

| Command | Explanation |
| --- | --- |
| `git switch -c <branch>` | Creates a new branch and switches to it. |
| `git switch <branch>` | Switches to the specified branch. |
| `git branch` | Lists the branches in the current repo. |
| `git branch  -a` | Lists the branches in the current and any remote repos. |
| `git branch <branch>` | Creates a new branch but does not switch to it. |
| `git merge <branch>` | Merges the specified branch into the current branch. |
| `git checkout -b <branch>` | Creates a new branch and switches to it. |
| `git checkout <branch>` | Switches to the specified branch. |
