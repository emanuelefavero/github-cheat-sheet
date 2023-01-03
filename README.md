# GitHub Cheat Sheet

Git and GiHub cheat sheet

### Common git problems cheat sheet

- [dangitgit.com](https://dangitgit.com/en)

## Create a new repository

1. `mkdir` or `cd` into the root directory of your project
2. `git init`
3. `git add .`
4. `git commit -m "first commit"`
5. Go to [GitHub](https://github.com/new) and create a new repository with name and description, then:
   `git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git`
6. `git push -u origin main`

## Create a new repository FROM THE COMMAND LINE

1. `git init`
2. `git add .`
3. `git commit -m "first commit"`
4. `gh repo create REPO-NAME --public -d 'description'`
5. `git remote add origin https://github.com/emanuelefavero/REPO-NAME.git`
6. `git push -u origin main`

## Subsequent adds, commits, pushes

1. `git add .`
2. `git commit -m "commit message"`
3. `git push`

## Open repo on github browser

- `gh browse`

## List all repositories

- `gh repo list -L 200`

## Tips

- Create a README.md file in the root of the repository
- Create a .gitignore file in the root of the repository
- Create a LICENSE file in the root of the repository

## Commit and push to GitHub

1.  `git add .`
2.  `git commit -m "commit message"`
3.  `git push -u origin main`

## Delete all local git files

- `rm -rf .git`

## Clone a repository

- `git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git`
  OR
- `gh repo clone YOUR_USERNAME/YOUR_REPOSITORY_NAME`

## Pull remote changes from GitHub to local

- `git pull`

## Create a new branch

- `git branch BRANCH_NAME`
  Or, to create a new branch and switch to it immediately:
- `git checkout -b BRANCH_NAME`

## Switch to a branch

- `git checkout BRANCH_NAME`

## See all branches

- `git branch`

## Delete a branch

- `git branch -d BRANCH_NAME`
  OR
- `git branch --delete BRANCH_NAME`

## Merge a branch

- `git merge BRANCH_NAME`

## See all commits

- `git log`

## See all commits in a branch

- `git log BRANCH_NAME`

## HARD Reset to a commit (WARNING: this will delete all commits after the commit you are resetting to)

- `git reset --hard COMMIT_HASH`

## HARD Reset to a commit, delete all local changes (WARNING: this will delete all commits after the commit you are resetting to) and force push to remote (WARNING: this will delete all commits after the commit you are resetting to on the remote)

BEWARE: _Don’t use this method if the github repo is being used by multiple users_

- `git reset --hard COMMIT_HASH`
- `git clean -f`
- `git push -f origin main`

## Show

File changes in directory:

- `git status`

  Changes in tracked files:

- `git diff`

  History;

- `git log`

  Who changed what and when:

- `git blame`

  Show commit:

- `git show COMMIT_HASH`

  Local branches

- `git branch`

## Revert

Undo to last commit

- `git reset --hard`

Undo a commit:

- `git reset --hard HEAD~1`

  Undo two commits:

- `git reset --hard HEAD~2`

Revert to specific commit:

- `git revert COMMIT_HASH`

## Resolve merge conflicts

View conflicts:

- `git diff`

View merge conflicts against base file:

- `git diff --base FILENAME`

View merge conflicts against your changes:

- `git diff --ours FILENAME`

View merge conflicts against their changes:

- `git diff --theirs FILENAME`

Discard a conflicting patch:

- `git reset --hard`
- `git rebase --skip`

After resolving conflicts, merge with:

- `git add FILENAME`
- `git rebase --continue`

## Display description and README.md of a repository

- `gh repo view`
- `gh repo view https://github.com/emanuelefavero/REPO-NAME.git`

## Get how many commits a day in a repo

- `git log --date=short --pretty=format:%ad | sort | uniq -c`

## Get how many commits a month in a repo

- `git log --date=short --pretty=format:%am | sort | uniq -c`

## Get how many commits a year in a repo

- `git log --date=short --pretty=format:%ay | sort | uniq -c`
