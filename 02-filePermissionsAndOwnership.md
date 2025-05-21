#In this file we will see some commands on file permissions and ownership

### 01. How do you make script.sh executable?

**`chmod +x script.sh`** -> converts into executable file for all three owner, group and others

**`chmod +x script.sh`** -> converts into executable file for only owner. 

_Note: use `g+` for groups and `o+` for others. you can combine them as well for example `ug+` or `go+` based on your requirement._

**`chmod 111 script.sh`** -> converts into executable file for only owner. 

_Note: `1` is the defined octate for execute permissions first 1 is for owners, second 1 represents group, third 1 represents others. based upon your usage assing 1 and to remove permission use `0`_

### 02. How do you change the owner of file.txt to user1?

_Note: Only root user has the access to change the owner and group of the file, so make sure you have permissions to root user_

**`chown user1 file.txt`** -> changes the owner of file.txt to user1

_Note: user -R flag if it is directory so that the owner will be changed to all files recursively_

### 03. How do you change the group of file.txt to group1?

_Note: Only root user has the access to change the owner and group of the file, so make sure you have permissions to root user_

**`chown :group1 file.txt`** -> changes the group of the file to group1

_Note: user -R flag if it is directory so that the owner will be changed to all files recursively_

### 04. How do you set permissions rw-r--r-- for file.txt using octal notation?

_Note: Octal notation for r -> 4, w -> 2, x -> 1, based on that we will give the permission to the above question_

**`chmod 644 file.txt`** -> assigns read, write permissions to the owner and read permission to group and others.

_Note: user -R flag if it is directory so that the owner will be changed to all files recursively_

### 05. How do you set read and execute permissions for the group on dir1?

**`chmod -R g+rx dir1`** -> sets permissions to read and execute for dir1 and files in dir1.

### 06. How do you recursively change permissions of a directory and its contents?

Ans: To change the permissions of a directory and its content recursively we can use -R flag to chmod command. **`chmod -R <permissions> <directory>`**

### 07. What does chmod 755 script.sh do?

Ans: The command will assign **read, write and execute permissions** to the **owner**. **read and execute** permissions to the **group and others**. so we can say that it converts script.sh to a executable file. 

### 08. How do you set the sticky bit on a directory?

_Note: Sticky bit is a special permission which is used to provide write permissions to all users but only the owner or privilaged user can rename or delete the files other people cannot delete._

**`chmod 1777 <file-path/dir-path>`** -> this will add sticky bit to directory to remove it use **`chmod -t <file-path/dir-path>`**

**`chmod +t <file-path/dir-path>`** -> use +t flag to add sticky bit.

### 09. How do you remove write permission for others on file.txt?

**`chmod o-w file.txt`** -> removes the write permission for others on file.txt.

### 10. How do you check the default umask value?

_Note: umask is the default permissions assigned to a file or dir while creation, by default the permissions for a file are 666 and dir are 777 if umask is 0022 then it will subtract 2 from group and 2 for other, so the file will get 644 and dir will get 755 permission. generally this umask is defined in /etc/profile /etc/bashrc ~/.bashrc ~/.bash_profile_

**`umask`** -> prints value in 4decimal format `ex: 0022` .it is default in most linux systems.

**`umask -S`** -> prints the output in human readable format.

### 11. How do you set the umask to 0022?

**`umask 0022`** -> This will set permission until the session after that it will be restored to default values..

_Note: add the umask 0022 /etc/profile and use source /etc/profile to permanently change the values, first 0 denotes the special permissions like sticky bit, set user id, set group id etc.,_

