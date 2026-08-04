# Git | GitHub Course

## Configuration and Editing Notes

`git config --global core.editor "code--wait"`: Allows commit messages to be added through VS Code Editor. 

> Path may need to be added in VS Code

> `CMD + Shift + P` then `"Shell Command: Install 'code' command in PATH"`

### Checking Git Username and Email
`git config --global user.name`: To check your git username on your terminal

`git config --global user.email`: To check your git email

### Setting Git Username and Email
`git config --global user.name "Your Name"`: To set your git username

`git config --global user.email "your@email.com`: To set your git email globally

`git config user.name`: Checks the setting for just the current repo 1(if you're inside one. and it's set differently than global)

`git config user.name`: Shows all git config settings at once, so you can grep for what you need. `git config --list | grep user`

### Amending Commits

Rather than making a branch new separate commit, you can "redo" the previous commit using the --amend option. 

`git commit --amend`

Replace the tip of the current branch by creating a new commit. 

### Git Ignore

You can tell Git which files and directories to ignore ina given repository, using a `.gitignore` file. 
This is useful for files you **NEVER** want to commit, including:
- Secrets, API Keys, Credentials
- Operating System Files (`.DS_Store` on Mac)
- Log Files
- Dependencies & Packages

Create a file called `.gitignore` in the root of a repository. Inside the file, we can write patterns to tell Git which files & folders to ignore:
- `.DS_Store` will ignore an entire directory
- `folderName/` will ignore an entire directory
- `*.log` will ignore any files with the `.log` extension

