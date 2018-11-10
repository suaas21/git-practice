Git Basics:
##############################

Extra information:
    1. $ echo 'My Project' > README.md (for creating README.md file)

Getting a git repository:
    we obtain a Git repository in one of two ways:
    1. $ git init 
    2. $ git clone <url>  (for existing reposotory)

Checking the Status of Files:
    1. $ git status 
    2. $ git status -s (use -s or --short for short status)
    3. $ git diff (for more information we get)

Tracking New Files:   
    1. git add .  (tracking all file)
    2. gir add <file1_name> <file2_name>
Ignoring Files:
    1. create .gitignore file then add into the file which we ignore
        example:
        *.[oa]   (ignore any files ending in “.o” or “.a”)
        *~         
Commit/snapshot files:
    1. $ git commit -m "message"

Removing Files in staging area:
    1. $ git rm <file_name> -f

Rename or Moving Files:
    1. $ git mv <file_from> <file_to>

git commit viewing:
    1. $ git log
    2.  $ git log -p -2 (view last 2 commit)

Undoing things:
    1. Undo commit:
        1. $ git commit -m 'initial commit'
           $ git add forgotten_file
           $ git commit --amend -m 'initial commit'
    2. Unstaging a Staged File:
        1. first create CONTRIBUTING.md then
            $ git add *                         (for staging)
            $ git reset HEAD CONTRIBUTING.md     (for unsatging)
    3. Unmodifying a Modified File:
        1. $ git checkout -- CONTRIBUTING.md

Working with Remotes:
    1. showing remotes:
        1. $ git remote
                origin 
        2. $ git remote -v
                origin  git@github.com:suaas21/git-practice.git (fetch)
                origin  git@github.com:suaas21/git-practice.git (push)
    2. Adding Remote Repositories:
        1. $ git remote add <remote_name> https://github.com/suaas21/git-practice (origin->remotr_name)
        2. $ git fetch <remote_name> ( downloads the data to your local repository — it doesn’t automatically merge it                                  with any of your work or modify what you’re currently working on)
    3. Pushing to Your Remotes:
        1. $ git push <remote> <branch>
    
    4. Inspecting a Remote:
        1. $ git remote show origin
    5. Renaming and Removing Remotes:
        1. $ git remote rename origin pb
        2. $ git remote remove origin       (remove origin repository)





