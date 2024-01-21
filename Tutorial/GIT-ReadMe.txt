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

Step 5: Check the Status of GIT
	git status
	Observe a message which reads untracked files. 
	
	
	