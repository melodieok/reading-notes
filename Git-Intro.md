# SETTING UP A GIT REPOSITORY

## Importing
1.  Switch to the target project’s directory
    * Example: $ cd test (cd = change directory)
2. Use the git init command
    * $ git init
3. To start tracking these repository files, perform an initial commit by typing the following:
    * $ git add *.c
    * $ git add LICENSE
    * $ git commit -m “any message here”

## Cloning

You can copy an existing Git repository from a server by using the clone command with a repository’s URL:

Example: $ git clone https://github.com/test

> When you clone a file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

## Workflow

The local Git repository has 3 components

1. Working Directory: The actual files reside here.
2. Index: The area used for staging
3. Head: Points to the most recent commit

## Life Cycle of File Status

1. When you edit a file, Git flags it as modified because of changes made after the previous commit.
2. Stage the modified file.
3. Commit staged changes.

## Helpful Commands

To determine the state of files, utilize the git status command:
  * $ git status

Track one file only by using the following format:
  * git add filename

Track all files in a repository by using the following command:
  * $ git add *

*After using these commands, files are tracked and staged for committing*

After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:

$ git status

On branch master

Changes to be committed:

  (use "git reset HEAD ..." to unstage)
new file: EXAMPLE
This information tells us that there are changes to be committed and that the file has been staged.

Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

$ git commit -m “made change x,y,z”
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

Committing All Changes
$ git commit -a
*This command commits a snapshot of all modifications to tracked files in the working directory.

Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

Example:

$ git push origin master
*This command pushes changes from the local “master” branch to the remote repository named “origin”.


# Q & A
What is Version Control?
  * a system that allows you to revisit various versions of a file or set of files by recording changes. You can modify a file or project to a previous version, track changes and users who made the changes as well
  
What is cloning in Git?
  * Cloning creates a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL
    
What is the command to track and stage files?
  * Track Single File command: git add filename
  * Track All Files command: $ git add *

What is the command to take a snapshot of your changed files?
  * $ git commit -a
  
What is the command to send your changed files to Github?
  * $ git push origin master
