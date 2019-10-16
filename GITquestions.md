# GIT Questions

*Q1. How can you check your current git version?*
 - [ ] git --v
 - [ ] git --current
 - [ ] git --options
 - [x] git --version
 
*Q2. What command would you use to create a new git repository ?*
 
 - [x] git init
 - [ ] git add
 - [ ] git start
 - [ ] git new
 
 Q3.  What will the following command print to the Terminal ?

     git remote -v

 - [x] A list of remote repositories you are connected to
 - [ ] The last 5 git versions you've installed
 - [ ] The current git version you're running
 - [ ] An inline editor for modifing remote repositories

Q4. How would you lookup information and statistics about a specific commit ?

 - [ ] git stat
 - [x] git show <commit> --stat
 - [ ] git debug --prettyprint
 - [ ] Query the remote repository with the commit hash.

Explanation :

Q5. If you run the following command from your master branch, what will happen ?
  
    git chechout -b beta-test

 - [ ] The beta-test branch will be checked out and deleted.
 - [ ] The beta-test branch will be checked out of the current commit.
 - [x] A new branch called beta-test will be created and switched to
 - [ ] The beta-test branch will be merged with the master branch

Explanation :

Q6. How could you squash multiple commits together without using **git merge --squash** ?

 - [ ] Rebashing
 - [ ] You can't. git merge --squash is the only git command for that operation.
 - [ ] Cashing
 - [ ] Reflogging

Explanation :

Q7.  Take a look at the git commands below and determine what the operation is doing ?

    $ git bisect start
    $ git bisect bad  54d4140abc4d2a76fdaab3w3sdfladfs
    $ git bisect good 69faa620daab3w3sabc4d2a7d2a76f

 - [x] Running a bisect that performs a binary search between two commits
 - [ ] Marking a commit as bad for later deletion
 - [ ] Marking a commit as good and resetting the HEAD
 - [ ] Running a merge that favors the commit marked good

Ans :

Q8.  After pushing commits to the remote repository for the first time using the command below, what shorthand command can you use in the future ?

    git push -u origin master

 - [ ] git push origin
 - [x] git push
 - [ ] same as before, git push -u origin master
 - [ ] git push master

Q9.  What is the status of the beta-notes.js file in the following output?
      
    Changes not staged for commit:
    (use "" git add <file>..."" to update what will be committed)
    ( use ""git checkout -- <file> ... "" to discard changes in wokring  directory)**
    modified : beta-notes.js

 - [ ] beta-notes.js is untracked and has been modified
 - [ ] beta-notes.js is untracked but has been added to the current commit.
 - [ ]  beta-notes.js is tracked, and the modified file has beed added to the current commit
 - [x] beta-notes.js is a tracked file and has been modified, but han not been added to the current commit

Ans : 

*Q10. After you've successfully merged two branches and commited the changes, What is the next step in keeping your git structure organized ?*

 - [ ] Use git reset --soft HEAD to roll back one commit
 - [ ] Run git rebase to move the current commit to its original location
 - [x] Run git branch -d to delete the merged branch
 - [ ] use git clear-all to cleanup any hanging files





Q11. Which of the following is true of the git push command ?

 - [x] By default a push doesn't send tags to the remote repository.
 - [ ] Commits can only be tagged when they are created
 - [ ] Only annotated tags are automatically pushed to the remote repository with a cimmit
 - [ ] Tags are pushed to the remote repository with their respective commits.

Q12. You're in the middle of modifying a file when you're unexpectedly assigned an urgent bug fix on another branch. What would you do to temporarily save the work your doing locally without commiting ?

 - [x] Use git stash to save your work and come back later and reapply the stashed commit.
 - [ ] You cannot save locally without committing , so this is not possible
 - [ ] Save your work with git local-cache.
 - [ ] Run git hold to save a local copy of what you're doing to return to later.

Q13.  How would you create a custom shortcut or command across your git environment?

 - [ ] Assign a shortcut or command using git options file
 - [ ] create a alias in the git config file
 - [ ] Run git hotfix with the shortcut name.
 - [ ] Use the git custom-key command.

Q14. What command lets you create a connection between a local and remote repository ?

 - [ ] git remote origin
 - [x] git remote add origin
 - [ ] git remote new origin
 - [ ] git remote add new

Q15.  What files is the following .gitignore programmed to leave out?
    
    # .swift
    build/
    *.txt
    *.metadata

 - [ ] Only files with .swift and .txt extensions.
 - [x] All files in the build directory, as well as files ending with .txt or .metadata
 - [ ] Only the build directory.
 - [ ] All file with  a .swift, .txt or .metadata file extension , as well as the entire build directory

Q16.  If you cloned an existing git repository what would happen ?

 - [ ] A copy of the repository would be created on the hosting platform
 - [x] A copy of the repository would be created on your local machine
 - [ ] A new copy would overwrite the central repository
 - [ ] Nothing cloning is not a supported git function

Q17. Suppose you needed to see a list of all files that had been modified or added to a specific commit over the course of a project. How would you accomplish this ?

 - [ ] Run git commit --info with the commit hash
 - [ ] find the commit in the remote repository, as that's the only place that kind of information is stored
 - [?] Use the diff-tree command with the commit hash
 - [ ] Access the commit stash data with git stash

Q18. Your current project has several branches; master, beta and push-notifications. You've just finished the notification feature in the push-notification branch, and you want to commit it to the beta branch. How can you accomplish this ?

 - [ ] Checkout the beta branch and run git merge push-notifications.
 - [ ] Checkout the master branch and run merge beta -> push-notifications
 - [x] checkout the push-notifications branch and run git merge beta
 - [ ] Delete the push-nofifications branch and it will be committed to the master branch automatically.

Q19. Why would you use a pre-receive hook in your remote repolitory ?

 - [ ] To invoke a hook script when commits are pushed but before any references are updated.
 - [ ] To debug all commit tags and release versions
 - [ ] To fire a script after updates are made to the remote repository
 - [ ] You wouldn't , you would use it in the local repository.



Q20.  What does the following command do to the git repository history ?

    git reset  --soft HEAD^

 - [ ] Deletes all previous commits and resets the repository history back to its initial state
 - [ ] Reset the working branch to the first commit
 - [ ] Keeps the HEAD at the current commit, but clears all previous commits
 - [ ] Undoes the last commit in the working branch and sets the HEAD back one commit.

Q21.  Looking at the following commands, describe what is happening.
       
       git checkout feature-user-location
       git cherry-pick  {af5597c29sdfjas7adjskdlfai34klad}

 - [ ] The commit is being tagged for release on the feature-user-location branch
 - [ ] A commit is being copied from its original branch over to the feature-user-location branch.
 - [ ] A commit is being copied from the feature-user-location to the master branch.
 - [ ] The commit is being cherry picked as the new HEAD of the commit history.

Q22.  What option can you use to apply git configurations across your entire git environment?

 - [ ] --all
 - [ ] --master
 - [ ] --update
 - [ ] --global
 
 Q23.Which of the following command is true when you use the followingcommand ?
      
      git add -A
 
 - [x] Only updated files are staged.
 - [ ] All new files are staged.
 - [ ] Files are staged in alphabetical order
 - [ ] All new and updated files are staged

Q24. After you make changes to a tracked file, you run the following command. What will this do ?

      git commit  -a -m "Refactor code base"

 - [ ] Adds all new files to the staging area
 - [x] Adds all modified files to the staging area then commits them with a message
 - [ ] Nothing, you can't use multple options in the same command
 - [ ] commits all new files with a message

Q25. You find a bug in your project, but can't locate where it was introduced in the commit history. How would you diagnose
this problem ?

 - [ ] Run a git rebase to find the buggy commit.
 - [x] Use git bisect to compare the buggy commit to an early commit that works as expected.
 - [ ] Manually backtrack through your commit history
 - [ ] Use git search -diff to compare all commits in your repository history.

Q26. What is the best way to characterize the git commit structure?

 - [ ] Data snapshot ?
 - [ ] Data log
 - [ ] Data dictionary
 - [ ] Data array

Q27.  Where are files stored before they are committed to the local repository

 - [ ] Saved files
 - [ ] git documents
 - [ ] git cache
 - [ ] Staging area
 
 Q28.  After checking your git status you get the following output, which shows the file beta-notes.js in the commit but also unstaged. How can this situation occur ?
 
     Changes to be commited :
     (use " git reset HEAD <file>..." to unstage)
     
     modified: beta-notes.js
     
     Changes not staged for commit:
     (use "git add <file>..." to updated what will be committed)
     (use "git  checkout -- <file>..." to discard changes in working directory)
     
     modified: beta-notes.js
     
 - [ ] There are two tracked copies of beta-notes.js, but one was removed from the commit.
 - [ ] Two copies of beta-notes.js were created , only one is being tracked.
 - [ ] There were tow copies of beta-notes.js, but one was deleted.
 - [ ] beta-notes.js was staged, then modified afterwards, creating two different versions of the file.
 
 Q29. Why would the followin command be used?
 
         git rebase -i HEAD~10
         
 - [ ] to delete the last 10 commits and resets the HEAD
 - [ ] in order to locally cache the last 10 commits
 - [ ] To run a comparative search of the last 10 commits for differences
 - [ ] To list the last 10 commits and modify them with either the squash or fixup commnad
 
 Q30. You've just restored some stashed commits you were  working on early,  but you want to carry them over into their own branch. How could you do that?
 
 - [ ] Add teh stashed commits to the current commit, then create a new branch.
 - [ ] Use git checkout -b .
 - [x] Run git stash branch <branch name>
 - [ ] git branch  <stash hash>
