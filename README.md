# Git-GitHub-Notes
## Basic Commands and Their Abbreviation:
- cd "change directory"
- mkdir "make directory"
- touch-> to create a file
- . -> current folder
- .. or ../ -> previous folder
- git int "git Initialise"
- ls "list" -> to show all files and folders
- la -> to show all files and folders including the hidden ones
- git clone **link** -> to put my remote repository (on GitHub) into my local machine (on device)
- git status -> to check the modification(changes)
- git add -> to add changes

## How to Initialise Git repository:
- Locally : use command "git init" on either Git Bash or Terminal.
- Remotely : go to GitHub -> 1. Create new repository
                             2. Add a new File
                             3. clone it using (git clone **link**)

## How to add changes to Staging Area:
- Before **commit** cd to root directory, type (git add --all / git add -A) for all the changes
- (git add .) stage changes within the current director
- Ways to add changes:
          -- git add --all
          -- git add -A
          -- git add .
          -- git add * (track all changes except the deleted ones)
          -- git add (file name)
          -- git add (file path i.e folder/file name)
          -- git add *.file extension ( to add all by file extension i.e ".txt" excluding deleted files or the files in the sub-folder)

## How to reset changes:
- before **commit** (git reset) in the root directory

## COMMIT:
**First and foremost add the changes to the stage them run**
- git commit -m "commit message"

## TO Login:
**If an error occur while committing like (PLease tell me who you are)**
