# The Git & GitHub Bootcamp

This README contains useful commands and notes from [The Git & GitHub Bootcamp by Colt Steele](https://www.udemy.com/course/git-and-github-bootcamp/ "Git & GitHub Bootcamp").

## Git

Git is a version control system that that tracks and manages changes to files over time. It allows you to:

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

### Table template

| Command | Description |
| ------- | ----------- |
