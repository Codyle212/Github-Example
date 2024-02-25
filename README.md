# Github-Example

github repo for programatice examples, .git in the project directory store all our git related information

### Versioning

- `git config --global user.email {email}` and `git config --global user.nane {name}` to configure git identity
- `git init` to initalize a repository and create a .git directory
- `git status` to check the current state of repository changes to file in git repo
- all files are untracked when they are not added to staging
- `git add .` or `git add {file}` to save changes to staging
- `git commit -m {message}` record the snapshot of tracked changes to the git repo
- `git remote add origin {remote_repo.gi}` to add remote connection to local git repo
- after adding the remote, a new remote entry will be added to `.git/config` file
- `git branch -m {old_branch} {new_branch}` will rename branch name
- `git push -u origin {current_branch}` will push the commited changes in current brances to remote repo
- `-u` flag of git push is the specify upstream
- `git log` shows all the previous commit in the current branch
- `--oneline` flag of git log will only show commit with messages
- `git show {commit_id}` shows the changes in the commit for each file
- `git pull` get the latest changes from the remote

### Branches

- `git branch -c {branch_name}` creates a new branch with branch_name
- `git branch -a` list all branches in the repo
- `git checkout {branch_name}` set the current branch to branch_name
- `git switch {branch_name}` change branch to branch_name
- `git rm {file}` to remove files from git repo and staging
- `git mv {file}` to rename file in git repo and staging
- `git merge {branch_name}` merges the commit of branch_name to current branch
- `git clone {remote_repo}` copy a remote git repository to local

### Rollback

- `git checkout {file_name}` revert the file back to how it was before changes
- `git diff` shows the difference in files we made changes to
- `git diff --cached` shows the changes to files that was staged
- `git restore --staged {file_name}` move the file back to before staging
- use git log to get commit id, `git diff {c_id_prev}..{c_id_current}` to see the difference between commits
- `git revert {commit_id}` makes a new commit to remove the content in commit_id
- `git revert HEAD` revert back to previous commit and HEAD will point at previous commit
- `git reset {commit_id}` will reset to the commit id without leave any history

# Github CLI

### Cloning

- run `gh repo clone Codyle212/Github-Example` to clone this repository

###

- run `gh repo create` to create a repository

- use `  gh repo create my-project --private --source=. --remote=upstream` to create a repo base on local directory
