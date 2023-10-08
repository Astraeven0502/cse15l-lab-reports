# Lab Report 1 - Remote Access and FileSystem (Week 1)
## 1. For `cd` command

**`cd` with No arguments**
---
![Image](1.cd(NoArgument).png)

The working directory is /home. The `cd` command change the working directory to the given path, no arguments means that is the relative path and change the working directory to "/home/(No Argument)" which is still "/home". And there is no error output because the argument is succesfully taken by cd command, even the path is still the same.

**`cd` with A Path To a Directory**
---
![Image](2.cd(PathDirectory).png)

The working directory is /home. Like I mentioned above, the `cd` command change the working directory to the given path, the given path here is "lecture1". So the working directory changed to "/home/lecture1", and we can see the "~/lecture1" before the dollar sign. And there is no error output because the command is valid(the directory exist) and successfully execute.

**`cd` with A Path To a File**
---
![Image](3.cd(PathFile).png)

The working directory is /home. Like I mentioned above, the `cd` command change the working directory to the given path, the given argument is "lecture1/Hello.java" which means go the "home/lecture1/Hello.java" directory, and "Hello.java" is a file not a directory. Because of that, we are getting a error says "Not a directory".


## 2. For `ls` command

**`ls` with No arguments**
---
![Image](4.ls(NoArgument).png)

The working directory is /home. The `ls` command is to list all the files and folders the given path, no arguments means that is the relative path and list all the files and folders in the working directory "/home/(No Argument)" which is "/home" so the only thing inside the "/home" is "lecture1" folder and that is why the output is "lecture1" in blue. And there is no error output because the argument is succesfully taken and execute with correct output by `ls` command.

**`ls` with A Path To a Directory**
---
![Image](5.ls(PathDirectory).png)

The working directory is /home. The `ls` command is to list all the files and folders the given path, the argument I have here is "lecture1" which is the relative path and equal to the directory "/home/lecture1". And there are some files and folders inside the path "/home/lecture1", so it output "Hello.class", "Hello.java", "messages" and "README". And there is no error output because the argument is succesfully taken and execute with correct output by `ls` command.

**`ls` with A Path To a File**
---
![Image](6.ls(PathFile).png)

The working directory is /home. The `ls` command is to list all the files and folders the given path, the argument I have here is "lecture1/Hello.java" which is a file so it print out the directory of that file. And there is no error output because the argument is succesfully taken and execute with correct output by `ls` command.


## 3. For `cat` command

**`cat` with No arguments**
---
![Image](7.cat(NoArgument).png)

The working directory is /home. The `cat` command is used to print the contents of one or more files given by paths, there is no argument are given so the terminal does not know what contents should print. There is no error message but the terminal seems crash because the next line does not have "[user@sahara ~]$" prefix.

**`cat` with A Path To a Directory**
---
![Image](8.cat(PathDirectory).png)

The working directory is /home. The `cat` command is used to print the contents of one or more files given by paths, the argument I have here is "lecture1" which is the relative path and equal to the directory "/home/lecture1". However, the cat does not accept directory path, it only takes the file argument so here the terminal print out an error message indicate that lecture1 "Is a directory".

**`cat` with A Path To a File**
---
![Image](9.cat(PathFile).png)

The working directory is /home. The `cat` command is used to print the contents of one or more files given by paths, the argument I have here is "lecture1/Hello.java" which is the relative path and equal to the directory "/home/lecture1/Hello.java". It is a file which is in the correct format so the terminal prints out the contents inside the "Hello.java" file. There is no error message since it successfully execute the command `cat` and print out the correct content inside "Hello.java".
