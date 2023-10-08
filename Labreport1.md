# Lab Report 1 - Remote Access and FileSystem (Week 1)
## 1. For `cd` command

**No arguments**
---
![Image](1.cd(NoArgument).png)
> The working directory is /home. The cd command change the working directory to the given path, no arguments means that is the relative path and change the working directory to "/home/(No Argument)" which is still "/home". And there is no error output because the argument is succesfully taken by cd command, even the path is still the same.

**A Path To a Directory**
---
![Image](2.cd(PathDirectory).png)
> The working directory is /home. Like I mentioned above, the cd command change the working directory to the given path, the given path here is "lecture1". So the working directory changed to "/home/lecture1", and we can see the "~/lecture1" before the dollar sign. And there is no error output because the command is valid(the directory exist) and successfully executed.

**A Path To a File**
---
![Image](3.cd(PathFile).png)
> The working directory is /home. Like I mentioned above, the cd command change the working directory to the given path, the given argument is "lecture1/Hello.java" which means go the "home/lecture1/Hello.java" directory, and "Hello.java" is a file not a directory. Because of that, we are getting a error says "Not a directory".
