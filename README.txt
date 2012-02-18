Install git.
-------------

(once on each machine)

Install it, then:

Configure git machine-wide:

git config --global user.name "Susan Herdina"
git config --global user.email sreherdina@yahoo.com


set up ssh key
------------------

(once ever:)
	create an ssh keypair using: 
		ssh-keygen -t -rsa -C "sreherdina@yahoo.com"

	cut and past content of the public key (the one ending in .pub) to the github website

(one on each machine)

	For each new machine, copy the files:
		~/.ssh/id_rsa
		~/.ssh/id_rsa.pub


create a new project
---------------------------

	create a git repo:

		mkdir <project name>
		cd <project name>
		git init

	put something in the repo

		<create README file>
		git add README.txt

			(or
				git add *    - all files and dirs in current dir
				git add .	- current dir and everything under it.
						- these are both the same
			)

		git commit -m "message"    - the quotes mean we can use spaces in the message

push this project to github:
------------------------------------

	(First time ever:)

		git remote add origin git@github.com:sherdina/my-first-git-repo.git
		git push -u origin master

	files are now visible on github at:

		https://github.com/sherdina/my-first-git-repo


On a new machine:
--------------------------

	* install git
	* copy the ssh files
	* clone the project:

		From the project web page, get the project's "git@github.com…" link onto your clipboard
		(you want the link for ssh access, not http or read-only)

		git clone <paste>

		Now you have all the files locally.

Daily routine
-----------------

	* Get changes from the repo:
		git pull
	   (notice no params are needed here - git knows where to pull from and push to)
	
	* edit files

	* view status:

		git status

	* add files you want to commit:

		git add <files or directories>

	* commit changes

		git commit -m "message"

	* push them to github:

		git push

	  (again, no params needed, git now knows to push to repo at github)

GUI clients
---------------

I've installed "gitx" for you. Launch it, open your project, you can click and browse around.

