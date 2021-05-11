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

But it seems to work only if you go one step down. After that, if you
try and recommit the file to GitHub it gives you an error that - 

'Failed to push .....rejected because the tip of your current branch is 
behind its remote counterpart. Integrate (e.g. git push etc...) and try
again.'


Was able to push a modified file using the LATEST commit from GitHub.
However, if you try doing the same process with a commit older than the
latest you get the 'Failed to push .....' error.

Now learning branching in GitHub. Lets see if able to resolve the earlier
push conflict using branching.

line to enter to Master Branch xxxx

When I opened this filee, the previous line 'Adding this line to master 
branch' was not there because this file is in the Learning_Branching 
branch and that line was added to the readme.txt file in the master 
branch.

File with 'Add this line to master branch xxxx' committed to GitHub Repo

Anyway, adding this line to the Learning_Branching Branch.
Learning_Branching

All the jibber jabber typed in the Learning_Branching readme.txt file does
not appear here.

After resolving conflicts - committed the readme file to main. So, merge
conflict resolved. 

Then merged main to Learning_Branching. 

When I tried to add and then commit - git status kept telling me nothing 
to add or commit. I pushed to GitHub anyway and then checked - both main 
and Learning_Branching versions of the file Readme.txt are the same.

Now - lets try - if I did the whole same process again - and only did merge -
on the learning_branch(after committed conflict resolved version to main) - 
would my conflict resolved changes appearing on main branch also show up on
the learning_branching branch. 

Above did not work - even if I did merge - no changes showing up on 
GitHub. I tried pushing without adding and commiting but that did not 
work either - nothing got pushed. Then finally went thru the process of 
adding, committing and pushing again. While adding and committing - it 
kept showing no files added or ready to commit. But when I pushed - it 
worked and my GitHub repository got updated - main and Learning_Branch 
was the same.

BUT something really interesting happened. - 

1. When I committed to the main branch - I had 22 commits. 2. Till this 
point - the learning_branching branch was still showing the unmerged 
file(I didnt pay much attention to this assuming a new commit would be 
made when I committed the conflict resolved file to the 
Learning_Branching branch - so I am not sure but I think the changes 
were still not reflecting). 3. Anyway, what I am sure of is that the 
number of commits remained 22 even after I now committed the merged 
resolved conflict file to the Learning_Branching branch as well. 4. This 
is in line with not being able to add or commit anything. BUT after add, 
commit and push - there was only one commit for the updated file and 
Learning_Branch and Learning_Branching shows me both main and branch are 
even. 

So, what happened here - did the push request overwrite my previous
commit on the Learning_Branch?

For deleting branches on local repo - 

checkout to different branch and then 

git branch -d branch_name

BUT to delete from GitHub - 
____________________________________
git push origin --delete branch_name

OR 

git push origin :branch_name

Where origin is the original (remote) directory where the branch was cloned
from.
