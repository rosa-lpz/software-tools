# Commits

## Create commit

```bash
# add file/folder
git commit -m "insert_comment"
```

## Remove a git commit that has not been pushed

I did a `git commit` but I have not pushed it to the repository yet. So when I do `git status`, I get '# Your branch is ahead of 'master' by 1 commit.

So if I want to roll back my top commit, can I just do:

```bash
 git reset --hard 6f1bfa856866809287a95d28a5f6f1a36d8a0201
 git reset --hard HEAD~1
```


### Reference

* https://stackoverflow.com/questions/1611215/remove-a-git-commit-which-has-not-been-pushed
* 

## Commit History

### Viewing the commit history

#### Command line

```bash
git log
```


```bash
git log --pretty="%h - %s" --author='Junio C Hamano' --since="2008-10-01" \
   --before="2008-11-01" --no-merges -- t/
5610e3b - Fix testcase failure when extended attributes are in use
acd3b9e - Enhance hold_lock_file_for_{update,append}() API
f563754 - demonstrate breakage of detached checkout with symbolic link HEAD
d1a43f2 - reset --hard/read-tree --reset -u: remove unmerged new paths
51a94af - Fix "checkout --track -b newbranch" on detached HEAD
b0ad11e - pull: allow "git pull origin $something:$current_branch" into an unborn branch
```

#### GitHub

In your GitHub repository:

1. Open the repository.
2. Click on commits (above the file list).
3. Find the specific commit.
4. Copy its commit SHA (hash).

### Fetch an previous commit

**Fetch commit locally**

```
git fetch origin
```

**Checkout the old commit**

```
git checkout <commit-hash>
```

This puts your repository in a detached HEAD state. You're viewing the code exactly as it was at that commit.

**To restore that old version as a branch (optional)**

```
git checkout -b old-version <commit-hash>
```

**To make the current branch match that old commit (optional)**

Warning: This changes the branch history.

```
git reset --hard <commit-hash>
```

GitHub to match (optinal):

```
git push --force-with-lease origin main
```

- 

# References

* https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History
* https://www.ivanontiveros.com/git-cheat-sheet/
* https://stackoverflow.com/questions/1611215/remove-a-git-commit-which-has-not-been-pushed