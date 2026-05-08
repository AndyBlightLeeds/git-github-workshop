# git-github-workshop

Git and GitHub workshop examples developed for UK RAS STEPS.

## Course outcomes

By the end of this course, participants should be able to:

- Understand what Git is and how it works.
- Use Git locally (`init`, `status`, `add`, `commit`, `log`, `branch`, `help`).
- Work alone or in a small team using GitHub.
- Contribute to an open-source repository on GitHub.

## 1) What Git is and how it works

Git is a distributed version control system:

- **Working tree**: your files on disk.
- **Staging area (index)**: a preview of what will go into the next commit.
- **Repository (`.git`)**: commit history and metadata.

```bash
# Show where your repository metadata lives
ls -la .git

# Inspect commit history graph
git log --oneline --graph --decorate --all
```

## 2) Local Git workflow examples

### Create a repository and first commit

```bash
mkdir hello-git
cd hello-git
git init
git status

echo "Hello, Git" > notes.txt
git add notes.txt
git commit -m "Add initial notes file"
git log --oneline
```

### Make changes and commit again

```bash
echo "Second line" >> notes.txt
git status
git add notes.txt
git commit -m "Update notes with second line"
git log --oneline --decorate
```

### Branching basics

```bash
git branch feature/readme-improvements
git switch feature/readme-improvements
echo "Branch-specific change" >> notes.txt
git add notes.txt
git commit -m "Add branch-specific note"

git switch main
git branch
```

### Built-in help

```bash
git help
git help commit
git commit --help
```

## 3) Working alone or in a team with GitHub

### Solo workflow (your own repository)

```bash
# after creating a repository on GitHub
git remote add origin https://github.com/<user>/<repo>.git
git branch -M main
git push -u origin main
```

### Team workflow with pull requests

```bash
git switch -c feature/add-training-exercise
# edit files
git add .
git commit -m "Add training exercise"
git push -u origin feature/add-training-exercise
```

Then on GitHub:

1. Open a Pull Request.
2. Request review.
3. Discuss feedback in comments.
4. Merge when checks/reviews pass.

## 4) Open-source contribution workflow

```bash
# 1) Fork on GitHub, then clone your fork
git clone https://github.com/<your-user>/<project>.git
cd <project>

# 2) Add original repository as upstream
git remote add upstream https://github.com/<owner>/<project>.git
git fetch upstream
git switch -c fix/docs-typo upstream/main

# 3) Make changes and commit
git add .
git commit -m "Fix typo in documentation"

# 4) Push to your fork and open PR to upstream
git push -u origin fix/docs-typo
```

## 5) Command-line `diff` and `patch` examples

### Example A: Use `diff` to compare two files

```bash
echo "version 1" > app-v1.txt
echo "version 2" > app-v2.txt
diff -u app-v1.txt app-v2.txt
```

### Example B: Create and apply a patch

```bash
mkdir patch-demo && cd patch-demo
echo "line 1" > sample.txt
cp sample.txt sample.txt.orig

echo "line 2" >> sample.txt

# Create patch file from original -> updated
diff -u sample.txt.orig sample.txt > update.patch

# Recreate original state
cp sample.txt.orig sample.txt

# Apply patch to get updated content back
patch sample.txt < update.patch
cat sample.txt
```
