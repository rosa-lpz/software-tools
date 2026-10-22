# Branches

## Common commands

```bash
git branch                      # List branches
git branch <branch-name>        # Create a new branch
git checkout <branch-name>      # Switch to a branch
git checkout -b <branch-name>   # Create and switch to a new branch
git branch -d <branch-name>     # Delete a local branch
```


## Clone in an specific branch

```bash
# Clone the specific branch using git clone with the -b flag
git clone -b branch_name https://github.com/username/repository
```

## Push to a branch created in local

To push the current branch and set the remote as upstream, use

```bash
git push --set-upstream origin <branch_name>
```

## Track remote branch already created

```bash
# to make sure your local branch has a [remote tracking # branch]
git push -u origin branchname
git remote add upstream github_repository_url
git branch --set-upstream-to branch_name
git branch --set-upstream-to main

```

**Add upstream**

```bash
git remote add upstream <git_repository_url>
```

**Remove upstream**

```bash
git remote remove upstream
git rm remove upstream
```

**Verify Upstream remote**

```bash
git remote -v
```

**Pull changes from main or another branch**

```bash
git pull upstream main
git pull upstream <branch_nem>
```

# Reference

* https://stackoverflow.com/questions/520650/make-an-existing-git-branch-track-a-remote-branch
* https://stackoverflow.com/questions/69374455/fetch-the-latest-changes-from-main-branch
