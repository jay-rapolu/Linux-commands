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

