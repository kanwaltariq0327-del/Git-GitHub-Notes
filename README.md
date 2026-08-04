# Git-GitHub-Notes
## Basic Commands and Their Abbreviation:
- cd " change directory "
- mkdir " make directory "
- touch-> to create a file
- . -> current folder
- .. or ../ -> previous folder
- git init " git Initialise "
- ls " list " -> to show all files and folders
- la -> to show all files and folders including the hidden ones
- git clone **link** -> to put my remote repository ( on GitHub ) into my local machine ( on device )
- git status -> to check the modification ( changes )
- git add -> to add changes ( more ways in detail below )
- git reset ->to reset staged changes
- git reset --hard ( to recover the deleted files )
- git commit -m " commit message "
- git reset HEAD~
- git rm file-name ( to remove/delete and add the change together )
- git rm -f file-name / git rm --force file-name ( to delete forcefully )
- git rm --cached file-name ( to delete from the staging area )
- git rm -r " recursive " folder-name ( to remove the folder including all the contents )
- git branch ( to see all branches )
- git branch new-name ( to create new branch )
- git checkout branch-name ( to enter the mentioned branch )
- git merge name-of-branch-to-merge -m ( to merge the branch mentioned into the branch that we're in )

## How to Initialise Git repository:
- Locally : use command -> **git init** on either Git Bash or Terminal.
- Remotely : go to GitHub ->
  1.Create new repository
  2.Add a new File
  3.clone it using ( git clone **link** )

## How to add changes to Staging Area:
- Before **commit** cd to root directory, type ( **git add --all / git add -A** ) for all the changes
- ( **git add .**) stage changes within the current director
- Ways to add changes:
  1.git add --all
  2.git add -A
  3.git add .
  4.git add * ( track all changes except the deleted ones )
  5.git add file-name
  6.git add file-path ( i.e folder/file name )
  7.git add *.file extension ( to add all by file extension i.e " .txt " excluding deleted files or the files in the sub-folder )

## How to reset changes:
- before **commit** run -> ( **git reset** ) in the root directory

## COMMIT:
**First and foremost add the changes to the stage them run**
- git commit -m "commit message"

**In order to roll back to the previous state**
- git reset HEAD~

### To watch commit history:
**In order to see a detailed log of the commit history**
- git log
 
**but if we want to see more cleaner version of this then**
- git log --oneline

## TO Login:
**If an error occur while committing like (Please tell me who you are)**
use the configuration command :
- git config --global user.email "email"
- git config --global user.name "name"

**configuration specific to a single file**
- git config --local user.email "email"
- git config --local user.name "name"

## Remove the File:
- If we want to delete a file ( not manually ) and automatically want to stage the change then we should run -> **git rm file-name**
- Changes made to the file and not committed cannot be deleted with the command above either commit it first then run the command or else **forcefully remove it using command ( git rm -f file-name )**
- run command **( git rm --cached )** to remove from the staging area and not the working directory
- In order to delete a folder including it content ( i.e any file or sub-folder ) run -> **git rm -r folder-name** it will also stage the changes

## BRANCHING:
**Branch is like a separate line of development where we can work independently** 
- **Main** is the default branch
- To ensure we do not ruin the work while testing or creating new features we create new branch **git branch new-name**
- when the new branch is created it inherits the current state of the branch that we were in e.g -> ( main ) --> git branch staging  **main == staging**
- any changes made in the separate branch will not affect the main branch unless committed and **merged**
- To merge one branch into another ( i.e merging the branch that we are in with the branch that we will mention in the command ) run command -> **git merge name-of-branch-to-merge -m ( -m to leave message )**
  1. e.g: ( main ) -> git merge staging -m "I've merged the staging branch with the main branch"
  2. Now all of the data of staging will be transferred to the main branch however, the staging branch will remain unchanged
- to enter a branch -> **git checkout name**
- In order to see all the branches or list of branches run -> **git branch**









