# Linux basic commands

_In this readme file you can find basic linux commands._

### 01. How do you list all files in a directory, including hidden files?

`ls -a` to list all the files.

`ls -A` to list all files excludes **'.'** and **'..'**.

`ls -al` to list all the files in long list format.

### 02. How do you display the current working directory?

To list the current working directory you can use **`pwd`** or **`echo $PWD`**.

### 03. How do you create a directory named projects?

**`mkdir projects`** -> creates in directory current directory.

**`mkdir /path/projects`** -> creates directory in the specified path. *Note: It will not create if path is not present*

**`mkdir -p /path/projects`** -> creates directory in the specified path and it will create path dir as well if it was not there.

**`mkdir -v /path/projects`** ->creates directory and prints the output message.

*Note: If you got any permission error use `sudo` and use it if you have access and sure about the path where to create and what to create*.

You can verify by using `ls -l` or `ls -d` if directory is created or not.

### 04. How do you delete an empty directory named temp?

*Note: You should have ***write permissions*** on the directory to delete.*

**`rmdir temp`** -> deletes an empty directory

**`rm -f temp`** -> deletes an empty directory.

**`rmdir -v temp`** -> deletes an empty directory and prints the output as well.

**`rmdir /path/temp`** -> deletes an empty directory using full path.

### 05. How do you rename a file from old.txt to new.txt?

**`mv old.txt new.txt`** ->rename old.txt to new.txt, this command is also used to move files from one location to other.

**`mv -n old.txt new.txt`** -> skips the file creation or rename if already a file exists with new.txt.

**`mv -i old.txt new.txt`** -> asks for a prompt before renaming the file.

**`mv -v old.txt new.txt`** -> prints the ouput once command is executed.

### 06. How do you display the contents of a file named notes.txt?

**`cat notes.txt`** -> to display full content in the file.

**`less notes.txt`** -> to display content in interactive way use scrollbar and keyboard arrows to view the file.

**`more notes.txt`** -> similar to less but can view page-by-page.

**`head notes.txt`** -> to view the top 10 lines of the file. Use *-n 5 tag* to print 5 lines and you can modify the number upon your requirement.

**`tail notes.txt`** -> to view the bottom 10 lines of the file. Use *-n 5 tag* to print 5 lines and you can modify the number upon your requirement.

:information_source: You can use -f in tail option to follow the files this option is mostly used in log files. to check real time logs.

**`tac notes.txt`** -> to view the file in reverse order only lines.

**`rev notes.txt`** -> to view the file in reversed characters in the same line order.

**`nl notes.txt`** -> to print the file along with the line numbers.

### 07. How do you create an empty file named test.txt?

**`touch test.txt`** -> Creates an empty file named test.txt.

:information_source: If the file exists it updates the timestamp and keeps the content intact.

**`> test.txt`** -> faster than touch 

:warning: overwrites the test.txt if already exists and all data will be lost. 

### 08. How do you view the manual page for the ls command?

**`man ls`** -> to view the manual page of ls.

### 09. How do you clear the terminal screen?

**`clear`** -> to clear the screen.

**`reset`** -> to fully reset the screen and remove and printing glitches.

**`ctrl + l`** -> shortcut to clear the screen.

### 10. How do you list files sorted by modification time?

**`ls -t`** -> to list the files by newest first.

**`ls -rt`** -> to list the files by oldest first.

### 11. How do you display the last 10 lines of a file?

**`tail -n 10 file-name`** or **`tail -10 file-name`** -> to display last 10 lines of a file.

### 12. How do you count the number of lines in a file?

**`wc -l file-name`** -> to list number of lines in a file.

### 13. How do you search for the word "error" in logfile.txt?

**`grep -i "error" logfile.txt`** or **`cat logfile.txt | grep -i "error"`** -> to search for word error in logfile.txt

### 14. How do you display the system’s hostname?

**`hostname`** -> use hostname command to display the hostname.

**`cat \etc\hostname`** -> by reading the hostname file

**`sysctl kernel.hostname`** -> using sysctl command.

**`uname -n`** -> using option -n to uname command.

**`echo $HOSTNAME`** -> by printing the shell variable.

### 15. How do you shut down the system immediately?

**`sudo shutdown now`** -> by using shutdown command.

**`sudo poweroff`** -> by using poweroff command.

### 16. How do you restart the system?

**`sudo reboot`** -> using reboot command.

**`sudo shutdown -r now`** -> by adding -r flag to shutdown command.

**`sudo shutdown -r +5`** -> to reboot after 5 mins.

### 17. How do you check the Linux kernel version?

**`uname -r`** -> using uname command by adding -r flag to it.

**`hostnamectl | grep Kernel`** -> by using the hostname and filtering the output.

**`cat /etc/version`** -> by viewing the version file in etc directory.

### 18. How do you list all environment variables?

**`env`** or **`printenv`**-> to print all environment variables.

### 19. How do you display the path of the ls command?

**`which ls`** -> use which command to display the path of any command.

### 20. How do you exit a terminal session?

**`exit`** -> using exit command.

**`logout`** -> using logout command.

**`Ctrl + d`** -> using shortcut.

**`kill -9 $$`** -> to forcefully exit from the terminal.

### 21. How do you append text "Hello" to file.txt?

**`echo Hello >> file.txt`** -> using echo and redirecting output to the file.

**`echo Hello | tee -a file.txt`** -> using pipe and tee command to append the content.

### 22. How do you display the calendar for June 2023?

**`cal 06 2023`** -> by using cal command and passing month and year as inputs or arguments.

### 23. How do you show the disk usage of files and directories?

**`du -sh file/directory`** -> by using su command.

### 24. How do you list all users on the system?

**`cat /etc/passwd`** -> by viewing the /etc/paswd file.

### 25. How do you display the current date and time?

**`date`** -> use date command to display current date and time.

### 26. How do you search for a previously used command in history?

**`history | grep -i command`** -> use the pipe and grep command to find previously used command in history

### 27. How do you repeat the last command with sudo?

**`sudo !!`** -> use sudo !! to run previous command with sudo

### 28. How do you create a symbolic link link.txt pointing to original.txt?

**`ln -s path/to/link.txt original/file/path/original.txt`** -> use ln -s command to create a symbolic link or soft link.

### 29. How do you list block devices (disks and partitions)?

**`lsblk`** -> to list all block devices

**`lsblk -f`** -> to list all block devices along with filesystem.

**`sudo parted -l`** -> to list all block devices and their partitions.

### 30. How do you display the system’s uptime?

**`uptime`** -> use uptime command to display the systems uptime.

**`top`** -> using top command.

**`cat /proc/uptime`** -> to view the uptime file.
