# Git/Github Tutorial

## Install Git

### Windows

To install git on windows go to https://git-scm.com/downloads and download the windows version of git

### Linux

To install git on linux search for console in apps and open it then run the commands

`sudo apt-get update` 
`sudo apt-get install git.`

One after the other

## Create a Github account

Go to https://www.github.com and create an account.

## Setup Git

Run the following commands on Git Bash (or console in linux) replacing the name with yours and the email with your github email

`git config --global user.name "John Doe"`
`git config --global user.email johndoe@example.com`

## Setup Github SSH key

Search for Git Bash (console in linux) and open it

![Search](images/git_bash_search.png)

![Bash](images/git_bash.png)

Run the following commands on Git Bash (or console in linux)

`ssh-keygen -t ed25519 -C "your_email@example.com"` - where the email is you github email

When asked for a password choose something you will remember

In github go to settings

![settings](images/git_hub_settings.png)

Then SSH and GPG keys
![settings](images/ssh_gpg_keys.png)

And then new SSH key
![settings](images/new_ssh.png)

Then Run the following command in commands on Git Bash (or console in linux)

`clip < ~/.ssh/id_ed25519.pub`

Then Ctrl+V in the Key field select type Authentication Key and give it whatever title you want

![settings](images/create_key.png)

And press Add SSH key

## Creating a repository on github

In your github profile in the Repositories section press New

![settings](images/github_create_repo.png)

Choose a fitting name and privacy policy for your repository

![settings](images/create_op.png)

Choose the proper gitignore for the language you are using, this will stop the repository from being filled with unnecessary files.

![settings](images/git_ignore.png)

## How to open console/terminal in a folder

### Windows 11 and linux

Right click in the folder and select console/terminal
![settings](images/open_teminal.png)

### Windows 10 and bellow

In path of the folder type `cmd` and press enter
![cmd](images/cmd.png)


## Using a repository

In your repository copy the ssh link
![settings](images/repo_ssh_2.png)

Open your terminal/console in the folder you want your repo to be in and type

`git clone ssh_link` - where the ssh_link is the link you copied
 
write your ssh key password when asked

![settings](images/clone.png)

Now you are free to add whatever documents you want in your repo

![settings](images/before.png)
![settings](images/after.png)

After you are ready to send the documents you made to the repo open the console inside the folder and type the commands

`git status` - to see what changes and comments haven't been added to the repo 

![settings](images/status.png)

`git add file_name` - to start tracking a certain file with git

`git add .` - to start tracking all files in the folder with git

![settings](images/add.png)

`git commit -m "message"` - to commit changes to repository (where message is a small summary of the changes you made, usually no longer than 20 words)

`git log --oneline` - to see what commits have been made

`git push` - to send all commits to the repository