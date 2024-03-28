# how-to-get-started-with-git
directions on uploading your first github project on your local machine to github.com using CLI

Reference this website: https://www.youtube.com/watch?v=wrb7Gge9yoE

1. download Github CLI; create a github repo on github.com
On the command line:
2. navigate to the folder your project is in on the command line
3. make this github local repo by: git init
4. stage the files for committing by: git add .
5. see the files you added by: git status
6. commit the files by: git commit -m "first commit"
7. go to github.com quick setup page of your new repo, and copy the remote https url for your github repo
8. on command line: git remote add origin <link> 
9. push local repo to repo on gihub.com by: git push -u origin master
a. if error: error: src refspec master does not match any
b.  then use: git push
c.  solution will be to do this instead (CLI will tell you also): 
1. To push the current branch and set the remote as upstream: git push --set-upstream origin main
  2. authenticate in the browser

created  June 6, 2023
  
  ----
  if you get error that file is too big, so you delete file, but git push still says you are committing that file: you need to clear your commit history:
  
  Deleting the .git folder may cause problems in your git repository. If you want to delete all your commit history but keep the code in its current state, it is very safe to do it as in the following:

Checkout

git checkout --orphan latest_branch

Add all the files

git add -A

Commit the changes

git commit -am "commit message"

Delete the branch

git branch -D main

Rename the current branch to main

git branch -m main

Finally, force update your repository

git push -f origin main

PS: this will not keep your old commit history around


----
For this same problem, the easiest thing to do is, 1. delete the large file from your local repo also - since you can't push it to github anyway. 2. undo the previous git add . command using: git reset --soft HEAD. 3. use git status, git add ., git push, to see if problem is resolved, if not, then undo 2x: git reset --soft HEAD~2. 4. do this process: try, git push, if error persists, then undo 3x and so on.






----
Now, how to create a new branch for each commit, and save to that branch:

When you are ready to commit, then first:

1. make a copy of current branch into a new branch then switch to it:
   a. ways to do this: if you are already on the old_branch that has the current project state (The one you want to copy):
      git checkout -b NEW_BRANCH_NAME 
   b. if you are not already on it: then:
git checkout old_branch
git branch new_branch

**sometimes you might need to first do a git pull to get the full current state onto the branch before you copy it.



3. now that you are on this branch, simply do as before:
   git add .
   git status
   git commit -m "message"
   git push

