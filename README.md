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

### Table template

| Command | Description |
| ------- | ----------- |
