Hello Git and GitHub

Lets test Git Diff


Lets try this again. (Was able to test git diff repository file against
staged file - but I followed the same procedure previously - wonder why it
didnt work before. Will test a couple of times more to see if can figure out.)

Now, going to try to see the difference between files modified in the 
repository but not staged. 

2nd trial of git diff between repo and staged. 

git diff        -----> Shows difference between file modified but not staged. 
git diff --staged    ------> Shows difference between file modified and staged. 

Once staged 'git diff' - doesnt seem to show difference between file modified
in the repository. Only last change against file in staged area. 


Further to last statement - basically, once staged, Git doesnt see any new
modification on the file (Unless a new one is made) versus the file already in 
working directory but it is able to track the difference between the last file staged
for commit. 


