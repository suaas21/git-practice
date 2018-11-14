# Git Basics:


* Extra information:
```
    $ echo 'My Project' > README.md  (for creating README.md file)
```
* Getting a git repository:
    we obtain a Git repository in one of two ways:
```
    $ git init 
    $ git clone <url>   (for existing reposotory)
```
* Checking the Status of Files:
```
    $ git status 
    $ git status -s  (use -s or --short for short status)
    $ git diff  (for more information we get)
```
* Tracking New Files:
```
    $ git add .  (tracking all file)
    $ git add <file1_name> <file2_name>

```  
* Ignoring Files:

    create .gitignore file then add into the file which we ignore
        
        example:
        *.[oa]   (ignore any files ending in “.o” or “.a”)
        *~         
* Commit/snapshot files:
```
    $ git commit -m "message"
```
  

* Removing Files in staging area:
```
    $ git rm <file_name> -f
```
    

Rename or Moving Files:
```
    $ git mv <file_from> <file_to>
```
    

* git commit viewing:
```
    $ git log
    $ git log -p -2 (view last 2 commit)
```

* Undoing things:
    * Undo commit:
        ```
           $ git commit -m 'initial commit'
           $ git add forgotten_file
           $ git commit --amend -m 'initial commit'
        ```
    * Unstaging a Staged File:

        first create CONTRIBUTING.md then
        ```
            $ git add *                         (for staging)
            $ git reset HEAD CONTRIBUTING.md     (for unsatging)
        ```
    * Unmodifying a Modified File:
        ```
        $ git checkout -- CONTRIBUTING.md
        ```

* Working with Remotes:
    * showing remotes:
        ```
        $ git remote
                    origin 
        $ git remote -v
                    origin  git@github.com:suaas21/git-practice.git (fetch)
                    origin  git@github.com:suaas21/git-practice.git (push)
        ```
      
    *  Adding Remote Repositories:
        ```
        $ git remote add <remote_name> 
                https://github.com/suaas21/git-practice (origin->remotr_name)
        $ git fetch <remote_name>   ( downloads the data to your local repository — it doesn’t 
                                      automatically merge it with any of your work or modify what you’re currently working on)
        ```
        
    * Pushing to Your Remotes:
        ```
        $ git push <remote> <branch>
        ```  
    * Inspecting a Remote:
        ```
        $ git remote show origin
        ```
       
    * Renaming and Removing Remotes:
        ```
        $ git remote rename origin pb
        $ git remote remove origin (remove origin repository)
        ```





