
# Installing Git
  1) You might already have git installed. To check whether you do, open your terminal, type "git --version", and press enter. If you have it installed, 
    the version you have will be returned. If it isn't your terminal will tell you. 
  2) Installing Git for macOS:
        - Install Homebrew.
        - Type `brew install git` in your terminal
        - Type `sudo port install git`
  3) Installing Git for Windows:
        - Refer to this [web page](https://git-scm.com/download/win)
# Logging in
  1) Type `git config --global user.name "your_username"` into your terminal to add your email.
  2) Type `git config --global user.email "your_email_address@example.com"` to add your email address.
  3) Type `git config --global --list` to check the configuration. 
# Choosing a Repository to Work In
  1) Choose a project that you have access to.
  2) Click on the **Fork** button in the top right.
  3) Create a namespace
# Clone a Repository
  1) Type `git clone <url>`. As an example, we'll do `git clone https://github.com/cathyim/git-tutorial-example.git`
  2) To view the file, go to the new directory : `cd git-tutorial-example`

# Branches
  1) Typically, we work on **branches** which are copies of the files on the repository. Creating a branch allows you to work on copies of the files without effecting the original ones. 
  2) Creating a branch:
        - Type `git checkout -b <name-of-branch>`. Do not use underscores when naming your branch.
  3) Switching branches:
        - Type `git checkout <name-of-branch>`
  4) Viewing differences: 
        - Type `git diff`
  5) Viewing changed files:
        - Type `git status`
  6) Add and commit changes:
        - Type `git add <file-name>` for all the files that you want to commit. 
        - Type `git status` to check whhich files you have selected to commit. 
        - Type `git commit -m "description of what the commit does"` to commit the files.
  7) Deleting branch changes:
        - Type `git checkout .`
  8) Adding changes to main branch:
        - Finally, when you're ready to add the changes you have made into the main branch, type `git checkout <default-branch>` to switch to the main branch. Then, type `git merge <feature-branch>` to **merge**.
# Stash
  1) You use **stashes** when you want to save your changes without having to commit just yet.
  2) Type `git stash`
  3) To reapply your stashed changes type `git stash pop`
  4) To view stash differences, type `git stash show`
  5) Clear your stash with `git clear stash`
  
# Exercise
  1) Now go back to the git-tutorial repo that we closed earlier. Create a branch and add your name and a random fact about you. To complete this exercise, merge the branches.