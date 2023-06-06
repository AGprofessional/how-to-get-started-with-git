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
8. on command line: git remote add origin <paste url> 
9. push local repo to repo on gihub.com by: git push -u origin master
  if error: error: src refspec master does not match any
  then use: git push
  solution will be to do this instead (CLI will tell you also): 
1. To push the current branch and set the remote as upstream: git push --set-upstream origin main
  2. authenticate in the browser

created  June 6, 2023
