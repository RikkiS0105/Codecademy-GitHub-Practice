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

It worked. We typed a line - We are trying to make this line disappear.

On typing git checkout HEAD Readme.txt - the last version of the file
stored on GitHub replaced the file in my local repository.

After we finish this section on Codecademy Learn Git - have to run an 
experiment to see what happens when

1. I modify a file, stage it, commit it but dont push it yet.
2. Modify a file and stage it but no commit. 
3. Modify a file but no stage or commit. 

What happens when I do git checkout HEAD filename at that point. 

Does it change all the versions of the file - in local repo, in
stage area and ready for commit area? Or only on Local repo. If 
only on local repo that means if I need to change the files in 
stage and commit area - I neccessarily have to change my local
repo version and then stage that file and then commit it (replacing the one
already in stage and commit areas)?

Now checking out git reset to unstage(remove from commit) a file staged for
commit

Syntax for that is - 

git reset HEAD filename

Now checking out git reset to stage to last commit for which syntax is 

git reset commit-SHA (first 7 characters of commit you want to reset to). 

It worked - First reset from the commit you want to reset to. This only
resets till the staging area/for commit. Use Checkout to change the file
in the working directory to the one pulled from commit. 


