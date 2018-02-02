---
title: Linux Cheat Sheet
date: 2018-02-01
bigimg: [{src: "img/pexels-photo-68562.jpeg"}]
tags: ["linux","cheat sheet"]
---

Here are some commands to refer back to when dealing with a Linux machine.

<!--more-->

```bash
# Reboot a machine
shutdown -h now
reboot

# disk space info.  The '-h' gives the data in human-readable values
df -h

# size of each file/dir and its contents in the current dir
du -hd 1

# command to find which dir has the most data
du -h --max-depth=1

# Find free memory on a system
free -m

# Find what processes are using memory/CPU and organize by it
top -o %MEM
top -o %CPU
# load average is 1/CPU for 1, 5, and 15 minutes

# Strace a process
strace -p <pid>

---------------

# change the user:group ownership of a file/dir
chown root:git <file_or_dir>

# make a file executable
chmod u+x <file>

# get Linux info
uname -a
lsb_release -a

---------------

# search for a file in a filesystem
find . -name 'filename.rb' -print

# locate a file
locate <filename>

# show files, 1 per line
ls -1

# see command history
history 

# search CLI history
<ctrl>-R

# run last command that started with 'his' (use 3 letters min)
!his

# create a new directory and all the subdirectories to its path
mkdir -p dir/dir2/dir3

---------------

# Send a command's output to file.txt, no STDOUT
ls > file.txt

# Send a command's output to file.txt AND see it in STDOUT
ls | tee file.txt

### GREP
# -B/A = show 2 lines before/after search_term
grep -B 2 -A 3 search_term <filename>

---------------

# Find the programs that are listening on ports
netstat -plnt
lsof -i -P | grep <port>


### Handle packages
# List packages
dpkg -l

# Find an installed package
dpkg -l | grep <package>

# Install a package
apt-get install <package>


# See all environment variables
env
```
