# The Git & GitHub Bootcamp

This README contains useful commands and notes from [The Git & GitHub Bootcamp by Colt Steele](https://www.udemy.com/course/git-and-github-bootcamp/ "Git & GitHub Bootcamp").

## Git

Git is a version control system that tracks and manages changes to files over time. It allows you to:

- Track changes over multiple files
- Compare versions of a project
- Revert to a previous version
- Collaborate and share changes
- Combine changes

The repository or repo is a workspace that tracks and manages the files in a folder. You must create a repo for each project.

Refer to the [Git documentation](https://git-scm.com/ "Git documentation") for full details about using Git.

## Terminal commands

### Navigation

| Command                 | Description                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **`ls`**                | List the contents of the current directory.                                                                       |
| **`ls <directory>`**    | List the contents of the selected directory.                                                                      |
| **`ls -a`**             | List all contents including hidden contents, for example, .git.                                                   |
| **`open .`**            | Open the current directory in Finder. Use `start .` for Windows.                                                  |
| **`open <directory>`**  | Open the selected directory.                                                                                      |
| **`pwd`**               | Print working directory, the current location.                                                                    |
| **`cd <directory>`**    | Change to the selected directory.                                                                                 |
| **`cd ..`**             | Move back one level.                                                                                              |
| **`cat <filename>`**    | Display the contents of the file.                                                                                 |
| **`code .`**            | Open the files in the current directory in VS Code. You must have already installed this command in the Terminal. |
| **`code <filename>`**   | Open the file in VS Code.                                                                                         |
| **`Command`** + **`k`** | Clear the terminal.                                                                                               |

### Files and directories

| Command                          | Description                                                                                                                              |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **`touch <filename.extension>`** | Create a file with this filename and extension in the current location. You can make multiple files, for example, touch red.txt blue.txt |
| **`touch <directory/file.ext>`** | Create the file in the selected directory.                                                                                               |
| **`mkdir <name>`**               | Create a new directory with the selected name in the current location. You can make multiple directories like with the touch command.    |
| **`rm <file.ext>`**              | Delete the selected file. You can delete multiple files like the touch command.                                                          |
| **`rm -rf <directory>`**         | Delete the selected directory.                                                                                                           |

## Git commands

### Status

| Command                 | Description                                                                         |
| ----------------------- | ----------------------------------------------------------------------------------- |
| **`git status`**        | Check the status of the current repo.                                               |
| **`git log`**           | View the details of all the commits in the current repo. Enter `q` to exit the log. |
| **`git log --oneline`** | Display abbreviated details of all the commits.                                     |
| **`git --version`**     | Check the Git version installed.                                                    |

### Initialising

| Command               | Description                                                                                                                                                                                                                                                |
| --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git init`**        | Initialise a new Git repo in the current location. Before running `git init`, use `git status` to ensure you are not currently inside an existing repo.                                                                                                    |
| **`git clone <url>`** | Retrieve all the files associated with the repository and copy them to your local machine. This initialises a new Git repository on your machine and gives you access to the full history of the project. Ensure you are not inside a repo when you clone. |

### Configuring

| Command                                               | Description                                                                                                                                                            |
| ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git config --global user.name “My Name”`**         | Set your username in Git.                                                                                                                                              |
| **`git config --global user.email myname@email.com`** | Set your email in Git.                                                                                                                                                 |
| **`git config user.name`**                            | Check what your username is set as.                                                                                                                                    |
| **`git config user.email`**                           | Check what your email is set as.                                                                                                                                       |
| **`git config --global core.editor "code --wait"`**   | Set VS code as the default editor. In VS code, you may need to enter `command` `shift` `P` and select `Install ‘code’ command in Path` for the default editor to work. |

### Committing

| Command                          | Description                                                                                         |
| -------------------------------- | --------------------------------------------------------------------------------------------------- |
| **`git add <file1> <file2>`**    | Add the file to the staging area ready to commit.                                                   |
| **`git add .`**                  | Stage all changes at once.                                                                          |
| **`git commit -m “message”`**    | Commit the change and create a checkpoint that includes your message.                               |
| **`git commit`**                 | Commit the change and create a checkpoint. Your default editor opens for you to write your message. |
| **`git commit -a -m “message”`** | Add and commit at the same time.                                                                    |
| **`git commit --amend`**         | Amend the previous commit. Change the message or include files you forgot to commit.                |

### Branching

| Command                          | Description                                                                                                              |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **`git branch`**                 | View all the branches in the project. The active branch is marked with an asterisk. Enter `q` to exit the branch window. |
| **`git branch <branchName>`**    | Create the new named branch based upon the current HEAD. You will not switch to the new branch.                          |
| **`git switch <branchName>`**    | Switch to the named branch.                                                                                              |
| **`git checkout <branchName>`**  | Switch to the named branch. Not commonly used anymore.                                                                   |
| **`git switch -c <branchName>`** | Create the new named branch and switch to it at the same time.                                                           |
| **`git branch -d <branchName>`** | Delete the named branch. You can’t be on the branch you want to delete.                                                  |
| **`git branch -m <branchName>`** | Rename the branch you are on.                                                                                            |
| **`git branch -v`**              | View all branches with the latest commit information.                                                                    |

### Merging

| Command                      | Description                                                                                                                                                                                                                                                                                  |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git merge <branchName>`** | Merge the named branch into the current branch you are on. Fast forward merges require no message, merge commits require a message to be entered. If there are conflicts, resolve the conflicts in the file, remove the conflict markers in the file, add your changes, and make the commit. |

### Using diff

| Command                                            | Description                                                                                                              |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **`git diff`**                                     | List all the changes in your working directory that are not staged for a commit.                                         |
| **`git diff HEAD`**                                | List all the changes in your working directory since your last commit (staged and un-staged changes).                    |
| **`git diff --staged`** or **`git diff --cached`** | List all the staged changes in your working directory.                                                                   |
| **`git diff HEAD <filename>`**                     | List all the changes in your working directory since your last commit (staged and un-staged changes) for the named file. |
| **`git diff --staged <filename>`**                 | List all the staged changes in your working directory for the named file.                                                |
| **`git diff <branch1>..<branch2>`**                | List the changes between the tips of branch1 and branch2.                                                                |
| **`git diff <commit1>..<commit2>`**                | List the changes between commit1 and commit2. Requires the commit hashes.                                                |

### Stashing

| Command                         | Description                                                                                    |
| ------------------------------- | ---------------------------------------------------------------------------------------------- |
| **`git stash`**                 | Stash all uncommitted changes (staged and un-staged) and revert changes in your working copy.  |
| **`git stash pop`**             | Remove the most recently stashed changes in your stash and re-apply them to your working copy. |
| **`git stash apply`**           | Keep the most recently stashed changes in your stash and re-apply them to your working copy.   |
| **`git stash list`**            | View what’s in your stash.                                                                     |
| **`git stash apply stash@{n}`** | Keep the stashed changes in your stash and re-apply the selected stash to your working copy.   |
| **`git stash drop stash@{n}`**  | Delete the selected stash.                                                                     |
| **`git stash clear`**           | Delete everything in the stash.                                                                |

### Viewing commits and restoring

| Command                                        | Description                                                                                                                                                                                                                                                                 |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git checkout <commitHash>`**                | View a previous commit. The HEAD becomes detached. Use the switch command to switch to any branch to re-attach the HEAD. Alternatively, use the switch command to create a new branch and branch off from the commit.                                                       |
| **`git checkout HEAD~<n>`**                    | View a previous commit that is the entered number of commits before the HEAD. The HEAD becomes detached. Use the switch command to switch to any branch to re-attach the HEAD. Alternatively, use the switch command to create a new branch and branch off from the commit. |
| **`git switch -`**                             | Switch to the last branch you were on and re-attach the HEAD.                                                                                                                                                                                                               |
| **`git checkout HEAD <filename>`**             | Discard any changes in the file and revert back to the HEAD at the last commit. Can enter `--` instead of `HEAD`.                                                                                                                                                           |
| **`git restore <filename>`**                   | Discard any changes in the file and revert back to the last commit.                                                                                                                                                                                                         |
| **`git restore --source HEAD~<n> <filename>`** | Discard any changes in the file and revert back to the specified commit.                                                                                                                                                                                                    |
| **`git restore --staged <filename>`**          | Remove the file from the staging area.                                                                                                                                                                                                                                      |
| **`git reset <commitHash>`**                   | Reset the repo back to the specified commit. The commits that followed are deleted but the changes are kept in the files in the working directory.                                                                                                                          |
| **`git reset --hard <commitHash>`**            | Reset the repo back to the specified commit. The commits that followed are deleted and the changes are deleted from the working directory too.                                                                                                                              |
| **`git revert <commitHash>`**                  | Create a new commit that undoes the changes from the specified commit. This is the preferred method when you are collaborating with others.                                                                                                                                 |

### Using remotes

| Command                                                 | Description                                                                                                                                                                                                                                                                     |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git remote`**                                        | View the remote name linked to this repo.                                                                                                                                                                                                                                       |
| **`git remote -v`**                                     | View the remote name and URL linked to this repo.                                                                                                                                                                                                                               |
| **`git remote add <remoteName> <URL>`**                 | Link a URL to the specified name for the remote. Origin is the conventional name for a remote.                                                                                                                                                                                  |
| **`git push <remoteName> <branchName>`**                | Push the specified branch from the local repo up to the remote.                                                                                                                                                                                                                 |
| **`git push <remoteName> <branchName1>:<branchName2>`** | Push the specified branch1 from the local repo up to the specified branch2 in the remote.                                                                                                                                                                                       |
| **`git push -u <remoteName> <branchName>`**             | Set the upstream of the current branch from the local repo to the specified branch in the remote. This allows you to use the `git push` command.                                                                                                                                |
| **`git branch -r`**                                     | View the remote tracking branches your local repo is aware of.                                                                                                                                                                                                                  |
| **`git checkout <remoteName/branchName>`**              | View the last known commit from the remote for the branch. Use `git switch -` to re-attach the HEAD.                                                                                                                                                                            |
| **`git switch <remoteBranchName>`**                     | Create a new local branch from the remote branch of the same name. This lets you work on branches that were only in the remote and not local.                                                                                                                                   |
| **`git fetch <remoteName>`**                            | Download changes from a remote repo into your local repo without automatically integrating them into your working files. This is useful if you are working on a local branch and don’t want it to be updated when you download changes to the same branch from the remote repo. |
| **`git pull <remoteName> <remoteBranchName>`**          | Download changes from a remote repo into your local repo and integrate them into your working files. Unlike fetch, this updates the HEAD branch with the changes from the remote. Whatever branch you are on, that’s where the changes will be merged into.                     |
| **`git pull`**                                          | Download changes from the default remote and tracking connection set for the current branch you’re on.                                                                                                                                                                          |

### Rebasing

| Command                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **`git rebase <branchName>`** | Rewrite commit history to move your current branch so that it begins at the tip of a specified branch. For example, move your feature branch so that it begins at the tip of the master branch. This is useful if you must keep merging the latest master branch commits into your feature branch and clutter it with merge commits. This can be used as an alternative to merging or as a clean-up tool. It will turn muddled commits between two branches into a simple linear set of commits. </br> </br>Never rebase commits that have been shared with others. If you’ve already pushed commits to a remote, don’t rebase them. |
| **`git rebase -i HEAD~<n>`**  | Enter interactive mode and recreate commits in the specified range. You can edit commits, add files, drop commits, and so on. This does not rebase the commits onto another branch. Instead, it rebases them onto the HEAD they are currently based on.                                                                                                                                                                                                                                                                                                                                                                              |

### Using tags

Tags are commonly used to mark version releases in projects. They must be pushed to remotes separately from your branches and files.

Semantic versioning standard: **major.minor.patch**

Major releases are significant changes that are not backwards compatible. Minor releases contain new features that are backwards compatible. Patches are bug fixes and other small changes. Refer to the [specification](https://semver.org/ "Specification") for more information.

| Command                                 | Description                                                                                                                                                                                                                                  |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git tag`**                           | View all tags in the current repo.                                                                                                                                                                                                           |
| **`git tag -l “*<searchTerm>*”`**       | View all tags that contain the specified term. Use asterisks around the term to allow any characters before or after the term.                                                                                                               |
| **`git checkout <tag>`**                | View a previous commit with the specified tag. The HEAD becomes detached. Use the switch command to switch to any branch to re-attach the HEAD. Alternatively, use the switch command to create a new branch and branch off from the commit. |
| **`git diff <tag1> <tag2>`**            | List the changes between the commits with the specified tags.                                                                                                                                                                                |
| **`git tag <tagName>`**                 | Create a lightweight tag referring to the commit the HEAD is referencing.                                                                                                                                                                    |
| **`git tag -a <tagName>`**              | Create an annotated tag referring to the commit the HEAD is referencing. Your editor will open for you to add more information. Alternatively, use `-m` to write the message like for a commit.                                              |
| **`git show <tagName>`**                | View the full details for the tag.                                                                                                                                                                                                           |
| **`git tag <tagName> <commitHash>`**    | Create a lightweight tag referring to the specified commit.                                                                                                                                                                                  |
| **`git tag -f <tagName> <commitHash>`** | Move the tag to the specified commit.                                                                                                                                                                                                        |
| **`git tag -d <tagName>`**              | Delete the tag.                                                                                                                                                                                                                              |
| **`git push <remoteName> <tagName>`**   | Push the specified tag to the remote.                                                                                                                                                                                                        |
| **`git push <remoteName> --tags`**      | Push all tags to the remote.                                                                                                                                                                                                                 |

### Using reflogs

Reference logs are stored locally and only for 90 days by default.

| Command                                              | Description                                                                                                                                                                                                                                                             |
| ---------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`git reflog show <reference>`**                    | Show the log of the specified reference (this defaults to HEAD).                                                                                                                                                                                                        |
| **`git reflog <name>@{qualifier}`**                  | Show the log of the specified reference. For example, use the command `git reflog main@{one.week.ago}` to see the relevant log.                                                                                                                                         |
| **`git checkout <name>@{qualifier}`**                | Checkout at the specified reference. For example, use the command `git checkout main@{one.week.ago}` to checkout the main branch from a week ago.                                                                                                                       |
| **`git diff <name>@{qualifier} <name>@{qualifier}`** | Show the differences in the files between the two references.                                                                                                                                                                                                           |
| **`git reset --hard <name>@{qualifier}`**            | Use this if you want to recover a commit you have deleted or rebased for a branch. You can also specify the hash value instead of the name and qualifier. The reflog is useful in this situation because it stores records of commits even after you have deleted them. |

## Using aliases

Enter aliases in the global `.gitconfig` file to apply them to all repos.

For example, to make the command `git s` run `git status`, enter the following:

```
[alias]
    s = status
```

| Command                                  | Description                                                                                |
| ---------------------------------------- | ------------------------------------------------------------------------------------------ |
| **`git config --global alias.s status`** | Using the terminal instead of editing the file, make the command `git s` run `git status`. |

Useful aliases:

- [GitAlias](https://github.com/GitAlias/gitalias "GitAlias")

- [Must Have Git Aliases](https://www.durdn.com/blog/2012/11/22/must-have-git-aliases-advanced-examples/ "Must Have Git Aliases")

## Git process diagram

![Process](https://github.com/ChrisJones8181/GitNotes/blob/image/images/GitProcess.png)

## Exercises

If your Git skills are a bit rusty, here’s the list of exercises from the course to practice:

- [Committing Basics Exercise](https://plum-poppy-0ea.notion.site/Committing-Basics-Exercise-3dc1ef1873ce45e68cedd2265710d7d8 "Committing Basics Exercise")

- [Branching Exercise](https://plum-poppy-0ea.notion.site/Branching-Exercise-b5460c881d56400cb046357d9a430bf8 "Branching Exercise")

- [Merging Exercise](https://plum-poppy-0ea.notion.site/Git-Merging-Exercise-0236a17f04c847159a38f5efa978ce2c "Merging Exercise")

- [Diff Exercise](https://plum-poppy-0ea.notion.site/Git-Diff-Exercise-f7829bd2783940cea14239022a6c37a9 "Diff Exercise")

- [Stashing Exercise](https://plum-poppy-0ea.notion.site/Stashing-Exercise-b6b4ac460c0a4798845de177fc1eb86d "Stashing Exercise")

- [Undoing Things Exercise](https://plum-poppy-0ea.notion.site/Undoing-Things-Exercise-d2fc1825dcc047c291a9a960848fdf71 "Undoing Things Exercise")

- [GitHub Basics Exercise](https://plum-poppy-0ea.notion.site/Github-Basics-Exercise-1c12200326db47d7890702017602d698 "GitHub Basics Exercise")

## Hashing

These commands are listed here for interest and understanding how Git works, they are not commonly used.

| Command                                                | Description                                                                                                                      |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| **`git hash-object <filename>`**                       | Return the unique SHA-1 hash that refers to the data object. Nothing is stored by this command.                                  |
| **`echo “<string>” <pipe> git hash-object --stdin`**   | Return the unique SHA-1 hash that refers to the string specified between the quotation marks. Nothing is stored by this command. |
| **`echo “<string>” <pipe> git hash-object –stdin -w`** | Return the unique SHA-1 hash that refers to the string specified between the quotation marks and store it in the objects folder. |
| **`git hash-object <filename> -w`**                    | Hash and store the file in the objects folder.                                                                                   |
| **`git cat-file -p <hash>`**                           | Display the data stored for the hash.                                                                                            |
| **`git cat-file -t <hash>`**                           | Display the type of data stored for the hash.                                                                                    |

## Atomic commits

Try to keep your commits focussed on a single thing, feature, or fix. This makes it easier to undo or rollback changes later and makes code easier to review.

## Gitignore

Create a `.gitignore` file in the root directory and list files and folders that shouldn’t be tracked. For example, `.DS_Store`, API key files, and dependency folders like `node_modules/`. Recommended files to ignore can be generated [here](https://www.toptal.com/developers/gitignore "Gitignore").

## Vim

You may need to use the Vim editor when working with Git. Here's some useful commands.

| Command   | Description                                                                     |
| --------- | ------------------------------------------------------------------------------- |
| **`:q`**  | Quit Vim.                                                                       |
| **`i`**   | Enter insert mode and type a message. Use the `Escape` key to exit insert mode. |
| **`:wq`** | Write and quit.                                                                 |
