# GIT UP AND RUNNING 

## Github 
1. Register for a Github account on[ github.com](github.com).
2. Remember your Username and Email used.

## Setting up Git on your machine.
1. Download [Git](https://git-scm.com/downloads) for your appropriate Operating System.
2. Go to any project directory or empty directory.
3. Click ``Shift + Right Click`` and procees to click on ``Git Bash``.
4. Type in ``git config --global user.name "username"`` in the terminal that opened, replace ``username`` part with your Github Username, click Enter.
5. Type in ``git config --global user.email "uemail"`` in the terminal that opened, replace ``uemail`` part with your Github Email, click Enter.

## Setting up SSH
1. ssh-keygen -t rsa -b 4096 -C ``"your_email@example.com"``, Replace it with your Github Email, press enter.
2. Proceed to press Enter Thrice.
3. Type in ``cat ~/.ssh/id_rsa.pub`` in the terminal, press Enter, Copy the result content onto your clipboard.
4. Go to [Github Account Settings, Navigate to``SSH and GPG keys``](https://github.com/settings/keys), or click on this link.
5. Login to your Github Account if required, and reopen the above link.
6. Click on ``New SSH Key`` on top right of the opened Page.
7. Enter any title under ``Title`` Field to remember.
8. Paste the copied content from Git Bash Terminal into the ``Key`` Field, Click ``Add SSH Key``.

## Using Git and Github
1. Open Git Bash Terminal, Type ``git init`` to make a local git repo.
   **NOTE : Use cd to Change Directory as needed.**
2. Use your fav IDE or Text Editor to work on your code or project as needed in your project directory that you just initialised in Git Bash
3. Use ``git add -A`` to **Stage** your files, for updating the repo.
   **NOTE : ``-A`` adds all the files in that directory, you can mention individual files with their names as well.**
4. check the status of changed you'll be making soon with ``git status``.
5. Commit all changes made with ``git commit -m "Message"``.
   **NOTE : replace Message with anything you want like 'initial commit',or so, this is mandatory.**
6. Now your **Local** git repo has been updated.
7. To update this Local repo into github, go to [Github](github.com),Click on Repositories under your profile icon, make a new Repo by clicking on the button Top right, Fill in necessary details, and create it.
8. Now an SSH link is shown in the form : ``git@github.com:username/projectname.git``, copy this link.
   **NOTE : if its not shown, click on the green Code button near the top, click on SSH and copy the shown link.**
9. Now come back to git bash, type in ``git remote add origin **Paste link you just copied**``, and press Enter, you just made a remote access to your empty repo on github, and the remote has the alias '**origin**'.
10. use ``git push --set-upstream origin main``, where 'origin' is remote, 'main' is the branch.
    **NOTE : you can skip --set-upstream part after the first time, and just use git push.**
11. Now your project files are pushed to repo on Github.
12. When working on the project next time use ``git pull`` to make sure you have the latest copy of the repo, incase others worked on it.

NOTE : 
1. you might have to fork, if you are working on pre-existing project from github.

2. Skip step 1 and instead use ``git clone git@github.com:username/project.git``,if you are working on pre-existing Github repo that you just forked to download a copy of the project on to your computer.

3. you can fork a repo by going to github repo link, clicking the ``fork`` button on top right of the page, this creates the fork/copy of the repo onto your account, then follow the said steps with this new forked repo from your account.

4. To contribute or merge your work on the fork to main repo, go to the main repo's link, click on the ``Pull Requests`` button next to ``Issues`` button, choose your forked repo branch on the right side, and click on ``Create Pull Request``, wait for the owner of the repo to validate your work and merge.
