# Git and Azure Repos
- Azure Repos support both GIT and TFVC (centralised version control system)
- Github supports only GIT

- For dotnet projects add the bin and obj directories to .gitignore file

Git Flow
Working Directory -> Staging -> Local Repo -> Remote Repo

# Git Basic Commands
git init
git config user.name sagar
git config user.email sagar@abc.xyz
git status
git add .
git log
git commit -m -a (Both stage and commit at the same time)

# Pulling and Pushing code to the remote repository
https://dev.azure.com
1. Create a new project - HelloWorldApp as project name of Basic project type
2. Go to the Repos section
git remote add origin https://Genesso@dev.azure.com/Genesso/HelloWorldAppDotnet/_git/HelloWorldAppDotnet
git remote -v
git push -u origin --all
git branch

After making changes to push to the remote repo use the following command
git push origin master

A developer can pull the changes of code using the following command
git pull origin master

# Branches and Merging
git pull origin master
git branch feature/f1
git checkout feature/f1
Edit the code
git status
git add . && git commit -m "Feature F1"
git checkout master
git merge feature/f1
git push origin master
git log

