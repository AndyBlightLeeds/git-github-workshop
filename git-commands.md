# Commands Used In The Workshop Exercises

## Diff Patch Exercise

| Command | Explanation |
| --- | --- |
| `cd <directory>` | `cd` is short for change to the given directory. |
| `diff -Naur <dir1> <dir2>` | Show the differences between the contents of two directories. |
| `cp -r <dir1> <dir2>` | Copy recursively (`-r`) from \<dir1> to \<dir2>>. |
| `ls -R` | List the contents of the current directory and recursively down through the directory tree. |
| `patch -p1 < ../update.patch` | Applies a patch to the current directory using differences from `stdin`.  The redirect `<` causes the contents of the patch file to be streamed into `stdin`. |
| `cat <file>` | Outputs the file to `stdout`.  `stdout` is normally set to the current terminal window. |
| `git status` | Displays the status of the git repository. |
| `git apply <patch file>` | Applies the contents of the \<patch file> to the tree in the same way that `patch` does. |

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

## Revisions Practical

| Command | Explanation |
| --- | --- |
| `git tag <tag_name>` | Adds a tag to the current revision using the given `<tag_name>`. |
| `git status` | Displays the status of the git repository. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the `<message>`. |
 `git checkout <name>` | Checks out the revision that is pointed to by the branch or the tag with the given `<name>`. |

## Branches Practical

| Command | Explanation |
| --- | --- |
| `git switch -c <branch>` | Creates a new branch and switches to it. |
| `git log` | Displays details about the commits on this bran in the repo. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the `<message>`. |
| `git log` | Displays details about the commits on this bran in the repo. |
| `git switch <branch>` | Switches to the specified branch. |
| `git switch -c <branch>` | Creates a new branch and switches to it. |
| `git status` | Displays the status of the git repository. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the `<message>`. |
| `git log` | Displays details about the commits on this bran in the repo. |
| `git switch <branch>` | Switches to the specified branch. |
| `git log` | Displays details about the commits on this bran in the repo. |
| `git merge <branch>` | Merges the specified branch into the current branch. |
| `git switch <branch>` | Switches to the specified branch. |
| `git status` | Displays the status of the git repository. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the `<message>`. |
| `git status` | Displays the status of the git repository. |
| `git commit -am "<message>"` | When enter is pressed, any modified files that Git knows about are committed the `<message>`. |
| `git log` | Displays details about the commits on this bran in the repo. |
| `git switch <branch>` | Switches to the specified branch. |
| `git merge <branch>` | Merges the specified branch into the current branch. |
| `git log` | Displays details about the commits on this bran in the repo. |

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
