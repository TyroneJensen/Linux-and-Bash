# common-linux-commands-data-engineering

# common-linux-commands

**command structure: command -option target (ls -lah /tmp)**

to see all commands available:

- cd /usr/bin
- ls - l

**Useful commands**

time and date:

- cal
- date

disk usage or file size:

- df -h
- du -sh \*

system information:

- top

Exploring:

- pwd (shows path)
- ls -lah
- cd / (goes to root of system)
- cd ~ (goes to root of user)
- which python3 (shows location of executable)

Viewing files:

- less /etc/passwd (view file with pagination)
- cat /etc/passwd (print file to screen)

Counting lines:

- wc -l /etc/passwd

Modifying files and directories:

- touch newfile.txt
- mkdir newdir
- mv newfile.txt newdir/ (move file to newdir)
- mv newfile.txt newfile2.txt (renaming file using move command)
- mkdir -p moredir/dir1/dir2 (create multiple directories)
- rm -rf moredir

Processes:

- ps
- ./sleeper.sh &
- fg 1

Learning through docker:

- https://github.com/docker-library/python/blob/5e580185c613edaf930fa6d23358235b950da0bd/3.11-rc/bullseye/Dockerfile
