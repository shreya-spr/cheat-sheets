description: Git is a version control system.  
</br>

# STEPS - 
- create repo through GitHub Desktop
- create a file there and then commit it, publish that repository
- Now open gitbash in that directory on your PC 
- make any file changes as you wish , add <file> , commit, push etc

# Suppose you want to initialize (git init) a new Github repository, and then add it to a new remote repository and then start adding and committing to the files being added from the current working directory.

Make sure that the current working directory is the directory that needs to be pushed to the open-source platform (GitHub).
git init
git remote add origin https://github.com/user/repo.git
git push -u origin master


# Stages 
- create a repo
- make code/file changes
- stage it 
- push it
  
# Basic git commands:  

## To check if git is installed in your system
`git`
## To make a new file
`touch <filename>`  
# To delete files  
`git rm <filename>`  
## To initialise a new repository
`git init`  
(to continue working on existing repo, open git terminal in that directory)  
  
  > Tip: To open git in a specified location, move tot the location -> right click -> 'Open Git Bash here' option  

## To stage files
`git add <filename>` OR `git add *` OR `git add -all` to move everything to the staging area  

## To commit these files  
'git commit -m "your commit message"`  

## To check current status  
`git status`  

## To see commit history of project  
`git log`  

## To 'push' these changes from local to remote repo  
`git push origin main` (assuming you're on main) OR  
`git push origin <branchname>`  

## To revert to previous commit  
`git reset <insert_commit_id_here`  
(This will make all commits before this to go back to the staging area)  

## To unstage staged files  
`git restore --staged <filename>`  

## To hide a few staged files
`git stash`  
(This is for when you have a few staged files, later you want a clean codebase and not let these interfere with changes. You will reuse these files later. It's like you're sending them backstage to be called later on.)  

### To bring back those changes 
`git stash pop`  
### To clear the changes or files in your stash  
`git stash clear`  
  
     
# Working with existing projects on GitHub, contributions etc
## Stages
- fork it -- means you have a _copy_ of the file with you
- clone it  
    'git clone <insert_repo_url_here>`
- create a new branch  
    ```
    git checkout -b <your_new_branch_here> 
    git checkout <branch>   (switches to that branch directly)
    ```  

- make changes
- stage it, commit
- push it, push it to your own branch first  
> Always create a new branch for every pull request!  

# Working with branches  
### To check which branch you're currently on  
`git branch`  
### To view all branches  
`git branch -a`  

