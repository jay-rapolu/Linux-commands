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

>You can use -f in tail option to follow the files this option is mostly used in log files. to check real time logs.

**`tac notes.txt`** -> to view the file in reverse order only lines.

**`rev notes.txt`** -> to view the file in reversed characters in the same line order.

**`nl notes.txt`** -> to print the file along with the line numbers.

### 07. How do you create an empty file named test.txt?

**`touch test.txt`** -> Creates an empty file named test.txt.

>If the file exists it updates the timestamp and keeps the content intact.

**`> test.txt`** -> faster than touch 

<code style="color: darkorange">overwrites the test.txt if already exists and all data will be lost. </code>

