# Github-Example

github repo for programatice examples, .git in the project directory store all our git related information

### Global Config

git config store the global configuration
use `git config --list --show-origin` to find location of configuration

### Remote

use `git remote add origin {remote_url}` to add a remote which later can be used to pull commits
if we are pushing to remote with no branch, use `git push origin {branch_name}`

### GitHub Authentication

use `git auth login` to configure github account

### Solve Conflicts

use `git merge main` to the local branch you work on before submitting a pull request

### Stashes

use `git stash {stash_name}` to put the staged files aside
use `git stash list` to check out all stashes
use `git stash pop` to bring the changes back
use `git stash apply {stash_name}` to apply the stash to the branch

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
- `git reset` will revert all the file changes being staged

# Github CLI

- run `gh auth login` to authenticate
- run `gh auth token` to get back a token
  change the Environment Variables GH_TOKEN to use a different token
- run `gh repo clone Codyle212/Github-Example` to clone this repository
- run `gh repo create` to create a repository
- use `gh repo create my-project --private --source=. --remote=upstream` to create a repo base on local directory
- use `gh repo delete {repo_name}` to delete repository
- run `gh repo set-default` to set the current working repo, thne repos spcific command can be run
- run `gh label list` to list all possible labels
- run `gh issue create --title {title} --body {body_text}` to create an issue
