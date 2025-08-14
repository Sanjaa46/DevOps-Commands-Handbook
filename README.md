# DevOps-Commands-Handbook

## 1. Linux Basics
### Navigation
- `pwd` - print current working directory
- `ls` - list files in the current directory
- `cd` - change directory
- `cd ..` - move one directory up
- `cd ~` - go to home directory
### File management
- `touch file.txt` - make a brand new file in the current directory
- `mkdir folder_name` - create new folder
- `cp source.txt destination.txt` - copy a file
- `mv oldname.txt newname.txt` - rename or move a file
- `rm file.txt` - delete a file
- `rm -r folder_name` - delete a folder and its content
### Premissions
- `chmod 755 file.sh` - change file premissions
- `chown user:group file.txt` - change file owner and group
- `ls -l` - list files with premissions and owner info

### Process Management
- `ps aux` - list all running processes
- `top` - interactive process viewer
- `kill PID` - terminate a process by PID
	- Viewing files: cat, less, head, tail
	- Package management: apt, dpkg
	- SSH basics: ssh, scp
	- System service: systemctl, service
## 2. Git Basics
### Setup
- `git config --global user.name "Your name"` - set your Git username
- `git config --global user.email "you@example.com"` - set your Git email
- `git config --list` - view current Git configuration
### Creating Repositories
- `git init` - initialize a new local repository
- `git clone https://github.com/user/repo.git` - clone an existing repo
### Tracking changes
- `git status` - see which files are staged, modified, or untracked
- `git add file.txt` - stage changes for commit
- `git commit -m "message"` - commit staged changes
- `git log` - view commit history
### Branching
- `git branch` - list branches
- `git branch new-branch` - create new branch
- `git checkout new-branch` - switch to a branch
- `git merge branch-name` - merge naother branch into current branch




2. Git Basics
	- Setup: git config
	- Creating repos: git init, git clone
	- Tracking changes: git add, git commit, git status, git log
	- Branching: git branch, git checkout, git merge
	- Remote: git push, git pull
	- Resolving conflicts
3. Basic DevOps Tools
	- Docker: docker run, docker ps, docker image, docker exec, docker log
	- Systemd: systemctl start/stop/restart/status
	- Cron jobs: crontab -e, crontab -l
	- Networking: ip a, ping, curl, wget
4. Tips and Best Practices
	- Aliases in .bashrc
	- Using man and --help
	- Common troubleshooting steps
