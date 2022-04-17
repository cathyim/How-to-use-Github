
# Installing Git
  1) You might already have git installed. To check whether you do, open your terminal, type 'git --version', and press enter. If you have it installed, 
    the version you have will be returned. If it isn't your terminal will tell you. 
  2) Installing Git for macOS:
        - Install Homebrew.
        - Type `brew install git` in your terminal
        - Type `sudo port install git`
  3) Installing Git for Windows:
        - Refer to this [web page](https://git-scm.com/download/win)
# Logging in
  1) To add/configure your username, using the `git config --global user.name "your_username"` command in your terminal. 
  2) To add/configure you email address, use the `git config --global user.email "your_email_address@example.com"` command.
  3) Use the `git config --global --list` command to check the configuration. 
# Choosing a Repository to Work In
A GIT repository contains a collection of files of various different versions of a Project. You can either create your own repository to work in or you can choose a pre-existing project that you have access to.

### Creating a New Project/ Git Repository
If you would like to create a new repository to create a whole new project:
  1) Open a new terminal and go into the directory that you would like to create a folder in.
  2) Let's do an example. Create a folder on your desktop:
  ```
  cd Desktop
  mkdir new-folder-name
  cd new-folder-name
  ```
  3) Initialize Git using the `git-init` command (type: `git init`).
  4) Now, you have created/initialized an empty git repository to work in.

### Working on a Clone a Repository
If you would like to work on an already-existing project, you want to `clone` the repository. Cloning basically copies all of the files in the repository that you are cloning, and provides you with your own space to work with them. To clone a repository:
  1) Type `git clone <url>`. As an example, we'll do `git clone https://github.com/cathyim/git-tutorial-example.git`
  2) To view the file, go to the new directory : `cd git-tutorial-example`

# How to Add Files to a Project
### Add files to folder
Now, let's add a file to the new repository we created.
  1) Create a file of any type with a text editor. 
  2) Let’s do an example, 
```
Hello World! This is our first repository file :)
```
  3) To check to see if the file was successfully saved in your folder, use the `ls` command while in your project directory.
  4) Check the status of your repository using the `git status` command.
  5) Now that we have saved the file in our folder, we must add it to our repository.
  6) Note: There are three trees in your local repository. The Working Directory, which is where your files are stored and changes are initially saved; the Staging Environment/Index, which stores changes changes that are ready to be committed; and the Head which stores the most recent commit. 
### Staging files
Now, we want to get our files to the Staging Environment so that our files can get ready to be committed.
  1) Using the `git add` command to add files to the Stage Environment. 
  ```
  git add new-folder-name
  ```
  2) Check to see if the file has successfully been added by using the `git status` command.
  ```
  git status
  ```
  3) Note: To add multiple files to the Staging Environment, use the `git add --all` command. 
### Committing files
Now, we want to commit the files.
  1) We commit our files by using the `git commit -m "description of what the commit does"` command.
  ```
  git commit -m "Adds first hello world file"
  ```
  2) Note: To view all of your commits, use the `git log` command.

# Branches
Typically, we work on **branches** seperate versions of your main branch. Creating a branch allows you to work on copies of the files without affecting the original ones. This is particularly useful when working with others. This way, multiple people can work on separate branches on separate tasks. The main or master brnach is where final changes are merged. 
### Creating a branch:
Use the `git branch <name-of-branch>` command. Do not use underscores when naming your branch.
          ```
          git branch <exciting>
          ```
### Viewing all branches:
To view all of the branches that you have in your repository, use the `git branch` command.
### Switching branches:
  1) We are currently in the main branch. Let's switch to the exciting branch. Use the `git checkout <name-of-branch>` command.
          ```
          git checkout exciting
          ```
  2) Let's add a new file to our exciting branch. Open your IDE and create a new file named exciting with the following content:
          ```
          It's very exciting to learn for to use GITHUB!
          ```
  3) Save, stage, and commit this file, just as we've learned in the previous section.
### Viewing differences: 
Use the `git diff` command to see the differences between your branches. 
### Viewing changed files:
se the `git status` command to view your changed files.
### Remember:
  1) Use `git add <file-name>` command for all the files that you want to commit. 
  2) Use `git status` command to check which files you have selected to commit. 
  3) Use `git commit -m "description of what the commit does"` command to commit the files.
### Adding changes to main branch:
Finally, when you're ready to add the changes you have made into the main branch, use the `git checkout <default-branch>` command to switch to the main branch. Then, use the `git merge <feature-branch>` command to **merge**.
# Stash
  1) You use **stashes** when you want to save your changes without having to commit just yet, using the git stash` command.
  2) To reapply your stashed changes type `git stash pop`
  3) To view stash differences, type `git stash show`
  4) Clear your stash with `git clear stash`
  5) Let's say you want to add a file name to your new-folder-name repository, but it's incomplete for whatever reason and you want to be able to come back to it.
  6) Save your file and add it using the `git add` command.
  7) Use the `git stash` command to temporarilty store your file to work on later. 
  8) Note: Files that are not being tracked cannot be stashed, so you must add your file before stashing it.

