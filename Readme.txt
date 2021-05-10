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
working directory but it is able to track the difference between the last
file staged for commit. 

Now lets try difference between repo/committed files. 

git diff HEAD --------> Shows difference between repo file and last committed
file (be it in repo or in staging area). 

so, in conclusion - 

git diff        -----> Shows difference between file modified but not staged. 
git diff --staged    ------> Shows difference between file modified and staged. 
git diff HEAD --------> Shows difference between repo file and last committed
file (be it in repo or in staging area). 

GitHub doesnt have Automatic Version numbers for files. Only commit numbers. 
However, if that is the case, you cannot get the difference between lets say commit 2
and commit 5, only git diff between last commit. So you can set github to do
Auto Version number. I dont need this for now - but once I finish learning Git
on CodeCademy would be a good idea to revisit and install auto version
numbers depending on my preferences. 

Now we are trying out Git Checkout. 

