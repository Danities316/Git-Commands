# Git-Commands
## Add an existing project to GitHub steps
To push a new project to an existing GitHub repository, follow these steps:
- Create a GitHub repository for the existing project
- Copy the GitHub URL for the new repo to the clipboard.
- Perform a git init command in the root folder of the existing project: 
  <br>git init
- Add all of the existing project’s files to the Git index and then commit: 
  <br>git add and git commit -m "Add existing project files to Git"
- Add the GitHub repo as a remote reference for the existing project: 
  <br>git remote add origin https://github.com/cameronmcnz/example-website.git
- Perform a git push operation with the -u and -f switches: 
  <br>git push -u -f origin master
- Verify that the existing project’s files have been pushed to GitHub.



## Create branch from an existing branch steps
- git branch new_branch_name(to create a new branch name)
- git checkout -b branch_name(to enter into the branch and start work in it)
- git checkout -b new_branch_name existing_branch_you_want_to_create_new_branch_name_into(To create a new branch(called new_branch_name) from a base branch(called existing_branch_you_want_to_create_new_branch_name_into) )
- See image below
![6qEWk](https://user-images.githubusercontent.com/12422620/203994571-cb41a334-5ef9-49a2-98bf-a762394670fa.jpeg)

## Working with a forked repository on my local machine and pushing changes back to my fork on GitHub and then to the main original repo
-  Fork the Repository:
-  Clone the Forked Repository to Your Local Machine: git clone <repository_url>
-  Set Up an Upstream Remote(You might want to set up a remote that points to the original repository (the one you forked from). This will allow you to fetch updates from the original repository)
  : cd <repository_name>
  git remote add upstream <original_repo_url>
- Create a New Branch: git checkout -b my-feature-branch
-  Make Changes(Make changes to the code or files in your local repository using your preferred text editor or development environment.)
-  Commit Your Changes: 
   git add .
   git commit -m "Add feature: my changes"
-  Push Changes to Your Fork on GitHub: git push origin my-feature-branch
-  Create a Pull Request (PR)(Visit my forked repository on GitHub and create a Pull request
-  Review and Merge(The maintainers of the original repository can review your changes and choose to merge them if they meet the project's guidelines.)
-  Sync with Upstream (Optional):
   git fetch upstream
   git checkout main
   git merge upstream/main


## made changes in a branch but haven't yet added or committed those changes, and you want to discard those changes without committing them
-  git status
-  git reset --hard(To discard all the changes in your working directory (including untracked files))
-  git status(to verify changes)

## how To merged main branch into a feature branch
- Ensure your feature branch is up to date:
  Before merging changes from the main branch, it's a good practice to ensure your feature branch is up to date with the latest changes from the main     branch. You can do this by fetching the latest changes from the main branch and rebasing your feature branch onto it. This helps in avoiding unnecessary conflicts during the merge.
  `
  -  git checkout feature_branch
  -  git fetch origin
  -  git rebase origin/main
    `

- Merge main branch into the feature branch:
  Once your feature branch is up to date, you can merge the changes from the main branch into your feature branch:
  `git merge origin/main
`
  This command will merge the changes from the main branch into your current feature branch.

-  Resolve any merge conflicts:
  If there are any merge conflicts during the merge process, Git will pause and ask you to resolve them. You'll need to manually resolve the conflicts in your code, commit the changes, and then continue with the merge process by running:
  `git merge --continue`

-   Test your changes:
    After merging the main branch into your feature branch, it's essential to test your changes to ensure everything works as expected.
    `git push origin feature_branch
`
