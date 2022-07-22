---
title: git  
description: Git is a version control system.  
---

</br>

# STEPS - 
- create a folder for your repo in your PC or...
- or create repo through GitHub Desktop
- create a file there and then commit it, publish that repository
- Now open gitbash in that directory on your PC 
- make any file changes as you wish , add <file> , commit, push etc

## Suppose you want to initialize (git init) a new Github repository, and then add it to a new remote repository and then start adding and committing to the files being added from the current working directory.

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
`git reset <insert_commit_id_here>`  
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
  
> git pull == fetch + merge 


## Working with branches  
### To check which branch you're currently on  
`git branch`  
### To view all branches  
`git branch -a` 

## Creaate a local branch and push it to GitHub    
  
  Make your branch first then:  
  
  ```bash
git push --set-upstream origin <branch-you-just-created>
```

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
 

## To get latest changes of a repo onto your forked repo  
`git remote add upstream`  

## Change the git init default branch name  

Don't want to have it called master?  
```bash
mkdir -p ~/.config/git/template
echo 'ref: refs/heads/main' > ~/.config/git/template/HEAD
git config --global init.templateDir ~/.config/git/template/
```

Since version `2.28` of `Git` this can be done using this command:

```bash
git config --global init.defaultBranch main
```

For more info:
[Highlights from Git 2.28](https://github.blog/2020-07-27-highlights-from-git-2-28/#introducing-init-defaultbranch)  


## Add tracking information to your work  
git branch --set-upstream-to=origin/<branchname>  
  

## Stop tracking a previously tracked folder

First add the folder to your `.gitignore` then remove the folder from
your local git tracking with:

```bash
git rm -r --cached <folder>
```

## Start tracking a previously un-tracked file

```bash
git update-index --no-assume-unchanged <file>
```
  
## Clone a repo and give it a different name  
```bash
git clone https://github.com/your-username/repo-name new-repo-name
```  
  
    
    ## How to read last commit comment?  
    ```
    git show  # fastest, but shows the diff as well. 
    git log -1  # fast and simple,  
    git log -1 --pretty=%B    # for just the commit message and nothing else
    ```


# Git ref log

Want to know what work you have done on a repo? Use `git reflog` to
displpay all the commits.

```bash
# show all changes for the last 90 days
git reflog show -a
# show changes with a date
git reflog --date=iso
```

https://stackoverflow.com/questions/17369254/is-there-a-way-to-cause-git-reflog-to-show-a-date-alongside-each-entry  
