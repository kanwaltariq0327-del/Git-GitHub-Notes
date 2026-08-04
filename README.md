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
- git reset HEAD~ ( to undo the last commit and move everything back to the working directory )
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
   - git add --all
   - git add -A
   - git add .
   - git add * ( track all changes except the deleted ones )
   - git add file-name
   - git add file-path ( i.e folder/file name )
   - git add *.file extension ( to add all by file extension i.e " .txt " excluding deleted files or the files in the sub-folder )

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

## BRANCHES:
### What is a Branch?
=> **" Branch is like a separate line of development where we can work independently "** 

### Default Branch:
- **Main** is the default branch

### Creating separate branch and Merging:
- To ensure we do not ruin the work while testing or creating new features we create new branch **git branch new-name**
- When the new branch is created it inherits the current state of the branch that we were in
    - e.g -> ( main ) --> git branch staging  **main == staging**
- Any changes made in the separate branch will not affect the main branch unless committed and **merged**
- To merge one branch into another ( i.e merging the branch that we are in with the branch that we will mention in the command ) run command -> **git merge name-of-branch-to-merge -m ( -m to leave message )**
    - e.g: ( main ) -> git merge staging -m "I've merged the staging branch into main branch"
    - Now all of the data of staging branch will be transferred to the main branch. However, the staging branch will remain unchanged
### Further Commands to use:
- to enter a branch -> **git checkout name**
- In order to see all the branches or list of branches run -> **git branch**

## MERGE CONFLICT:
### What is a merge conflict?
- " When an exact same line of a file is changed in two different branches simultaneously then, version control system like Git cannot automatically combine changes from different branches thus occurs a **merging conflict**. "
         - i.e: Both lines have been modified, staged and committed in their respected branches.
         - e.g: let topic = " React " from ( main ) and let topic = " JavaScript " from ( staging )
         - Now we merge them using command.
         - Git will show an **error** stating something like: " Automatic merge fails, fix conflicts and then commit the result " 

### How to solve a MERGE CONFLICT?
- **" In order to solve a merge conflict we to need to adjust the changes manually to tell the system which version we want to keep and which to be discarded "**
- Git will itself point out the same lines that are causing the conflict
- We will remove the lines that we do not want and keep it simple as it was
- Then add the change ( with **git add .**) to the stage and run commit ( with **git commit -m " commit message " )
- After doing so merge the branches again **it will resolve the conflict**













