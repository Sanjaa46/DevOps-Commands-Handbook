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
	- Remote: git push, git pull
	- Resolving conflicts

## 3. Basic DevOps Tools
### Docker
- `docker run -it image_name` - run a container interactively
- `docker ps` - list running containers
- `docker ps -a` - list all containers
- `docker images` - list docker images
- `docker exec -it container_name bash` - enter a running container
- `docker logs container_name` - view container logs
- `docker stop container_name` - stop a container
- `docker rm container_name` - remove a container
### Systemd / systemctl
- `systemctl status service_name` - check the status of a service
- `systemctl start service_name` - start a service
- `systemctl stop service_name` - stop a service
- `systemctl restart service_name` - restart a service
- `systemctl enable service_name` - enable a service to start at boot
- `systemctl disable service_name` - disable a service from starting at boot
### Cron Jobs
- `crontab -e` - edit the current user's cronjobs
- `crontab -l` - list the current user's cron jobs
- `* * * * * command` - cron job format: minute hour day month weekday command
	- Example: `0 2 * * * /home/user/backup.sh` -> run backup,sh exery dat at 2:00 AM
- `systemctl restart cron` - restart the cron service (if needed)
	- Networking: ip a, ping, curl, wget
## 4. Tips & Best Practices
### Linux Tips
- Use `man command` or `command --help` to read the manual.
- Use tab completion to save typing and avoid mistakes.
- Create aliasing in `.bashrc` for frequently used commands.
	Example: `alias ll='ls - lah'`
- Use `history` to see past commands and reuse them.
### Git Tips
- Commit often with clear messages.
- Use branches for new features or experiments.
- Pull latest changes from remote before starting work.
- Resolve merge conflicts carefully and test before merging.
### DevOps Tips
- Keep Docker conatiners loghtweight; remove unused images/containers.
- Use systemd services to manage critical applications.
- Schedule cron jobs thoughtfully; log outputs to files for troubleshooting
- Document any scripts or commands you create for future reference.
