Once on each machine
-------------------------------
Install git.

Configure git machine-wide:

git config --global user.name "Susan Herdina"
git config --global user.email sreherdina@yahoo.com


Once to start a new project
------------------------------------

To create a new local git repo:

	mkdir <project name>
	cd <project name>
	git init


put something in it

	<create README file>
	git add README.txt
		(or
			git add *    - all files and dirs in current dir
			git add .	- current dir and everything under it.
					- these are both the same
		)
	git commit -m message
	


Then to make a copy of that repo on github

