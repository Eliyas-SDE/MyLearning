***********************************************************
-----------Distributed Version Control System--------------
***********************************************************


GIT is a software to be installed in your local machine.

GITHUB is a centralized repository where the entire project code will be pushed.
GITHUB manages the source code history.

GIT Terminology:
---------------
Checked-in  --> Files/Code pushed into the repository
Checked-out --> Entire repo will be mirrored into the local system and it acts as a backup of the repository.

GIT download link- https://git-scm.com/download/win 
Select GitBash during installation

To check GIT is installed:
==========================
Open GITBash command promp from windows and run:  
git config --list


Steps to configure GIT:
=======================
Note:	TO get GIT Help run git help config
*****

Step 1: Setup username
	git config --global user.name "Eliyas F"

Step 2: Setup user email
	git config -global user.email "eliyas.sde@gmail.com

Step 3: Name your default branch
	git config --global init.default branch main


Step 4: Initiate/Define a normal folder which could be your workspace into a GIT repository
	git init 
	Now observe a .git folder is newly created inside your workspace location. If you don't find .git folder then check the "Hidden Items" from the "View" option in the "Menu" bar


GIT commands:
============
git status
**********
	Observe a message which reads untracked files. 

git branch -m master main
*************************
	Now point your master brach to your main branch which you named at Step 3
	
git branch
**********
	Will say which branch the repo is currently pointing to eg. main or backup
	
git branch backup
*****************
	Creates a new branch called backup
	
git switch backup
*****************
	Now GIT will point to backup branch
	
git branch -d backup
********************
	Delete the branch backup
	
git add .
*********
	Add a file/folder you wish to track by GIT
	
git add ReadMe.txt
******************
	If you want to add a specific file
	
git rm --cached ReadMe.txt
***************************
	If you don't want your file to be tracked
	

.gitignore file
===============
	Create a file with .gitignore extension and Save As the same as "gitignore". Any file name or extension mentioned inside this file will not be tracked.
	eg. if *.JPG is added then no .JPG file present in the parent folder will be tracked.
	

commit:
======	
git commit -m "Commit my changes"
*********************************
	commit is something stored in the local repository. It stores the data as set of snapshots. It saves only the files which has been modified.
	
git commit -a -m "Add and Commit my changes"
********************************************
	add and then commit the changes

git log
*******
	Will return the last commit details like username, email, description etc
	
git diff
********
	Will return which file has been modified and what information is added/deleted.
	
git log -p
**********
	Will return the consolidated results of git log and git diff
	
	
merge
=====
git merge -m "Merge from main branch" main
******************************************
	This command will copy the recent changes from main to backup branch and the local repository must point to the target brach backup.


Push Code into the Distributed Repository:
==========================================
git remote add origin https://github.com/Eliyas-SDE/MyLearning.git
******************************************************************
	Establishing connection between your local and distributed repo.

git branch -m main
******************
	Linking your main branch to the distributed repository.

git push -u origin main
***********************
	Pushing your code to the distributed respository.
		
git fetch
*********
	Copies only the changes from the remote repository.

git pull
********
	Its a combination fo fetch and merge from origin/remote repository.

git push --all
**************
	Pushes both main and backup braches into the centralized repository
	
git pull https://github.com/Eliyas-SDE/MyLearning.git backup
************************************************************
	This will pull all the changes does exists in centralized repository and in the same branch backup
