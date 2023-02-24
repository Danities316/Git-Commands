# Git-Commands
## Add an existing project to GitHub steps
To push a new project to an existing GitHub repository, follow these steps:
- Create a GitHub repository for the existing project
- Copy the GitHub URL for the new repo to the clipboard.
- Perform a git init command in the root folder of the existing project: git init
- Add all of the existing project’s files to the Git index and then commit: git add and git commit -m "Add existing project files to Git"
- Add the GitHub repo as a remote reference for the existing project: git remote add origin https://github.com/cameronmcnz/example-website.git
- Perform a git push operation with the -u and -f switches: git push -u -f origin master
- Verify that the existing project’s files have been pushed to GitHub.



## Create branch from an existing branch steps
- git branch new_branch_name(to create a new branch name)
- git checkout -b branch_name(to enter into the branch and start work in it)
- git checkout -b new_branch_name existing_branch_you_want_to_create_new_branch_name_into(To create a new branch(called new_branch_name) from a base branch(called existing_branch_you_want_to_create_new_branch_name_into) )
- See image below
![6qEWk](https://user-images.githubusercontent.com/12422620/203994571-cb41a334-5ef9-49a2-98bf-a762394670fa.jpeg)
