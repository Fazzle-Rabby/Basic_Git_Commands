# Basic_Git_Commands

*** Welcome to git basic commands


-- Update your repository
$ sudo apt-get update


-- Install git
$ sudo apt install git
$ git --version
$ git help config
$ git config --help


-- Link git to github
$ git config --global user.email "frparvez9@gmail.com"
$ git config --global user.name "Fazzle-Rabby"


-- Add SSH key in github account
$ ssh-keygen
enter
enter
enter
$ cd .ssh/
$ ls
$ cat id_rsa.pub
copy the key
[Go to github account > setting > ssh and gpg key > new ssh key > title (ssh1) > key (paste)> save]


-- Back to home directory
$ cd


-- Check directory
$ pwd


*** Push and Pull command


-- Create local directory
$ mkdir Git


-- Move directory
$ cd Git


-- Initialize this directory as a local git repository
$ git init


-- Join github ongoing project
$ git clone (github https/ssh link paste)


-- Create file for new project
$ touch Basic_Git_Commands.txt


-- Check file
$ ls


-- Edit file
$ echo Welcome to git basic commands> Basic_Git_Commands.txt


-- check status (which file are added to index and are ready to commit)
$ git status


-- Again edit file
$ vim Basic_Git_Commands.txt
press i
press Esc
press :wq


-- Untrucked to trucked file (add files to index)
$ git add Basic_Git_Commands.txt


-- Commit the file (it refers to recording snapshot of the repository at a given time)
$ git commit -m "first commit"

-- Go to o github account > repositories > new > name (Basic_Git_Commands) > public > add a READEME.FILE > create repository > code > copy ssh link


-- Added remote repository to local repository
$ git remote add origin (paste https/ssh link)


-- file transfer remote to local repository
$ git pull origin master


-- if get error
$ git pull origin master --allow-unrelated-histories


-- file transfer local to remote repository
$ git push origin master


*** Multiple commit


-- Create multiple file
$ touch parvez1.txt
$ echo welcome to parvez1.txt> parvez1.txt
$ touch parvez2.txt
$ echo welcome to parvez2.txt> parvez2.txt
$ touch parvez3.txt
$ echo welcome to parvez3.txt> parvez3.txt


-- check status (which file are added to index and are ready to commit)
$ git status


-- Untrucked to trucked file (add files to index)
$ git add -A


-- Commit the file (it refers to recording snapshot of the repository at a given time)
$ git commit -a -m "commiting 3 files together"


-- Get stores history
$ git log


*** Branching


$ git branch firstbranch
$ git checkout firstbranch   (switch branch)
$ touch parvez4.txt
$ echo firstbranch file> parvez4.txt
$ git add parvez4.txt
$ git commit -m "first commit on branch"
$ ls
$ git checkout master
$ ls


*** Merging


-- Our destination masterbranch
$ git checkout master
$ git merge firstbranch
$ ls
$ clear
$ git checkout firstbranch
$ vim parvez4.txt
$ git commit -a -m "modified"   (tracked file so only commiting)
$ cat parvez4.txt      (show modification)
$ git checkout master
$ cat parvez4.txt     (modification has not affected in the masterbranch)


*** Rebasing


-- One kind of linear merging
$ git checkout firstbranch
$ touch parvez5.txt
$ echo welcome to parvez5> parvez5.txt
$ touch parvez6.txt
$ echo welcome to parvez6> parvez6.txt
$ git add -A
$ git commit -a -m "adding for rebasing"
$ ls
$ git checkout master
$ ls
$ git rebase firstbranch
$ ls
$ clear


*** Push to remote directory github


$ git checkout firstbranch
$ git push origin firstbranch
$ git checkout master
$ git push origin master


*** Revert beck to previous changes


$ touch revert.txt
$ echo revert> revert.txt
$ git add revert.txt
$ git commit -m "revert commit"
$ vim revert.txt   (revert revert)
$ git commit -a -m "2nd revert commit"
$ cat revert.txt
$ git log
[copy the first hexadecimal digits from "revert commit" log]
$ git checkout (paste) revert.txt
$ cat revert.txt
