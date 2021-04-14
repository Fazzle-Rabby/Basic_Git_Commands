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


-- check status
$ git status


-- Again edit file
$ vim Basic_Git_Commands.txt
press i
press Esc
press :wq


-- Untrucked to trucked file (add current directory)
$ git add Basic_Git_Commands.txt


-- Commit the file
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
