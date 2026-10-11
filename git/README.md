# Git
* Commits
* Branches

# Status

```bash
git status
```
# Starting a project


```cmd
git init                        # Initialize a new repo in the current folder
git clone <repo-url>            # Clone an existing repo
```


# Git Log

```bash
git log
```

# Add / remove file or folder

```bash
# add file/folder
git add <file_name> or <folder> 

# remove file/folder
git rm <file_name> or <folder>

# remove recursivly with -r
git rm r- <folder> 
```
# Restore

```bash
# to discard changes in working directory / unstage
git restore <file>
git restore --staged <file>
```



# Push
Push commits to branch

```bash
git push
```


# Tracking Git ignore



## Stop tracking - Using git rm -cached

**File**

```bash
git rm --cached file.zip
git commit -m "Stop tracking data.zip"
git push
```

Now, `data.zip` will be ignored by Git.



**Folder**

```bash
git rm --cached data/
git commit -m "Stop tracking data.zip"
git push
```

Now, `data.zip` will be ignored by Git.



## Stop tracking - Modifying gitignore file

Another effective way to untrack a folder is to modify your `.gitignore` file. This file tells Git which files or folders to ignore when tracking changes. Here’s how to do it:

1. Open or create the `.gitignore` file in the root of your repository.
2. Add the folder name you want to untrack.

```bash
echo "folder_name/" >> .gitignore
```

Output:

```text
folder_name/
```

After adding the folder to the `.gitignore` file, you need to untrack it using the `git rm --cached` command:

```bash
git rm -r --cached folder_name
```

Output:

```text
Unstaged changes after reset:
M   folder_name/file1.txt
D   folder_name/file2.txt
```

By adding the folder to the `.gitignore` file, you ensure that Git will ignore any future changes to that  folder. This is particularly useful for folders that contain temporary  files or build artifacts that you don’t want to include in your version  history.

Once you’ve made these changes, remember to commit your updates:

```bash
git commit -m "Add folder_name to .gitignore and untrack it"
```

This will finalize the untracking process and ensure that your repository remains clean and organized.



https://www.delftstack.com/howto/git/git-untrack-folder/

# User
```bash
git config --global user.email "you@exmaple.com"
git config --global user.name "Your name"
```

# References

* https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History
* https://www.ivanontiveros.com/git-cheat-sheet/
* https://stackoverflow.com/questions/1611215/remove-a-git-commit-which-has-not-been-pushed
* https://www.delftstack.com/howto/git/git-untrack-folder/
* https://stackoverflow.com/questions/520650/make-an-existing-git-branch-track-a-remote-branch
