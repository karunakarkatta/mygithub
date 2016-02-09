# mygithub 

Source code version control (Git) is mandatory in any Development/Test project. It can maintain the history of each file along with different versions.

Server IP: 192.168.1.3

Now on-wards we maintain common source code repository instead of having individual copy of source code.  

Git server can communicate with client systems using ssh(secured shell) protocol. Before using the version control server you have to generate a ssh key in your local system and send it to the version control server. once your key is configured on the git server than you can start downloading and working on the source code.

Procedure to create ssh key and transfer to server:
Step1: run the following command and press enter key for 3 times. It will create .pub file in your home directory.
		# ssh-keygen 
Step2: Rename .pub file with your name. 
	        # mv ~/.ssh/.pub ~/.ssh/<yourname>.pub"
Step3: send the .pub file by mail to me. I will configure  it on the git server.


Install git:
------------
sudo apt-get install git

1. Creating a new repository:
	 git init
 	 vim abc.c
 	 git add abc.c 
         git status
2. Commit history
         git log -p
         git commit -m "1st commit"
	 git log
         git status
         vim abc.c 
         git commit -a -m "2nd commit"

          git diff 3438cdde09b539d8693560c7eb61a289e77a1b1b d26a0d5de11646b4cba2746fac7c731c787fed3f
  	  git diff 3438..d26a
  	  vim abc.c 
  	 git status	
  	 git add abc.c
  	 git commit -m "3rd commit"
 	  git log --pretty=oneline --abbrev-commit

3. Git configuration: user settings

  661  git config user.name "Karunakar Reddy K"
  662  git config user.email "karunakar.es@gmail.com"

4. Shortcut: How to add changed files when committing
 git commit -a -m "2nd commit"

5. Throwing changes away
	git reset HEAD <file name>

6. Seeing the diff between commits

	show 3720b35

7. Configuring git: colored console output

 git config --global color.ui auto

8. git tag <name> <commit> assigns a tag to a commit. If <commit> is omitted, the last commit gets tagged:

  	git tag working 3438cd
  	git tag 
	git tag broken
 	git tag v1.0.3
	git log --oneline --decorate

9. Branches
  	git brarnch 
 	git log
  	git log --pretty=oneline --abbrev-commit
  	git tag
  	git diff working..broken
  	git status
  696  git log
  697  git branch newfeature
  698  git branch -v
  699  git log
  700  git branch
  701  vim abc.c
  702  git status
  703  git commit -a -m "new branch commit"
  704  git log
  705  git checkout master
  706  git log
  707  git status
  708  git log
  709  git branch
  710  git checkout newfeature
  711  vim abc.c
  712  git status
  713  git commit -a -m "new bug fixed"
  714  git log

10. Merging 

  715  git checkout master
  716  git merge newfeature
  717  git log
  718  git branch
  719  git branch -d newfeature
  720  git log
 
