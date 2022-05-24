## GIT

GIT is the most widely used version control system. It allows you to work in a decentralized way.

**Main uses**

- History
- Store code
- Teamwork
- See when an error was introduced

As a general rule we will use **Git BASH** as the console.

**Some commands to configure Git are:**

- git --version: Used to see the version of GIT installed
- git config --global user-name "Example": It is used to put a name.
- git config --global user.email example@gmail.com: Used to put an email.
- git config --global core.editor "code --wait": It is used to open an editor and with wait the terminal will wait until we close it.
- git config --global -e: In this way we can see the configuration file.
- git config --global core.autocrlf true: We will use true for windows and input for MAC. This configuration is used to automate the CR and LF properties.

**Workflow:**

This consists of 4 phases (computer, stage, commit, server).

**Basic GIT commands:**

- ls: Used to view the folders and files in the directory.
- pwd: Used to see the directory where you are.
- cd "folder": Used to direct us to a specific directory.
- cd ..: Used to exit the current directory.
- mkdir "folder": Used to create a new directory.
- git init: Used to initialize a repository in the current directory.
- ls -a: It has the same function as "ls" but with this we can see the hidden files and directories.
- code .: Used to open the edition of the folder you are in.
- git status: Used to see the status of the files.
- git add "example.txt": Used to send the selected files to the stage phase.
- git add .: It is used to send all the files to the stage phase.
- git restore "example.txt": Used to discard changes to the file.
- git commit -m "Descriptive comment": Used to commit the changes.
- rm "example.txt": Used to delete a file.
- git rm "example.txt": It is used to delete a file and do the "git add" directly.
- git restore --staged "example.txt": Used to cancel the git add and remove it from the stage.
- mv file1.txt file.txt: Used to rename the file
- git status -s: It is used to see the status in a summarized way.
- git diff: It is used to see the text or the modifications in a clearer way.
- git log --oneline: It is used to see the commit history along with the message that we have placed when doing each one.
- cat file.txt: It is used to see the content of the file in the console.
- git push: Upload files that have been committed.

**Ignore files and directories**

To ignore files and directories we must create a folder called ".gitignore" and there add all the files or folders that we want.

**Branches**

Branches are used to work on the code without making changes to the main branch.
We will have several commands:
- git branch: Indicates the branch you are on.
- git checkout -b "branch name": Used to create a new branch.
- git checkout main: It is used to change the branch, in this case to main.
- git merge branch: It is used to join the branch to the main branch. To do this we must be in the main branch.

**Upload to the cloud**

With this option we can upload our work to the cloud.
We will use the command "git remote add origin https://github.com/person/example.git" to link our git account to our local repository.
To upload the files to the cloud we will use "git push -u origin main". After doing this we must access with our user and a password that will be a token obtained in github.

**GITIGNORE**

There are some files that we should ignore:
- Log files
- Files with API keys/secrets, credentials, or sensitive information
- Useless system files like .DS_Store on macOS
- Generated files like dist folders
- Dependencies which can be downloaded from a package manager

You can ignore files on different ways, for example, if you want to ignore a file, that's the easiest pattern, is a literal file name. Also you can ignore entire directories putting / on the end.

The symbol * is used to match 0 or more characters (except /). With this command if you write *.java you will ignore all java files.
You can also use ? to match a specific character and ! to negate a file that shouldn't be ignored. For example: If you use *.java to ignore all java files but you don't want to ignore a specific file you can use !example.java, but you can't negate a file inside a directory such doing !files/example.java
Double asterisk ** can be used to match any number of directories.

You can have one .gitignore file or some .gitignore files in each directory to ignore specific things in each one.
