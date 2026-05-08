# git-github-workshop

Git and GitHub workshops developed for UK RAS STEPS.

## Course examples

Use these practical examples as guided exercises during the course.

### 1. Create a repository and first commit

1. Create a new repository on GitHub.
2. Clone it locally:
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```
3. Add a README and commit it:
   ```bash
   echo "# My Workshop Repo" > README.md
   git add README.md
   git commit -m "Add initial README"
   git push origin main
   ```

### 2. Work safely on a feature branch

1. Create a branch and add a change:
   ```bash
   git switch -c feature/add-introduction
   echo "Welcome to the workshop" >> README.md
   git add README.md
   git commit -m "Add workshop introduction"
   ```
2. Push the branch and open a pull request:
   ```bash
   git push -u origin feature/add-introduction
   ```

### 3. Keep your branch up to date

Before raising or updating a pull request:

```bash
git switch main
git pull origin main
git switch feature/add-introduction
git merge main
```

If there are conflicts, edit the file, then:

```bash
git add <file>
git commit
```

### 4. Review and merge via pull request

1. Open the pull request on GitHub.
2. Request a review from a teammate.
3. Respond to feedback with additional commits.
4. Merge using **Squash and merge** once approved.

### 5. Undo common mistakes

- Undo unstaged changes:
  ```bash
  git restore <file>
  ```
- Unstage a file:
  ```bash
  git restore --staged <file>
  ```
- Revert a pushed commit safely:
  ```bash
  git revert <commit-sha>
  git push origin main
  ```

### 6. Tag a release

```bash
git tag -a v1.0.0 -m "Workshop example release"
git push origin v1.0.0
```
