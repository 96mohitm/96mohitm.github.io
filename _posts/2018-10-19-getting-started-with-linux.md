---
layout: "post"
title: "Getting Started with Linux"

---


So you want to enter the world of free open-source operating systems.


# Top 11 commands you should know to get started with linux.

Listed here are the most frequent and basic commands that you need to know if you are getting started with linux. 

## 1. ls

This command is used to list all the directories and filies that are present in the current directory.

{% highlight shell %}
$ ls
{% endhighlight %}


## 2. cd

This command - change directory - is used to change between the directories.

{% highlight shell %}
$ cd foldername
{% endhighlight %}


## 3. mv

This command is used to move a file to another directory. 

The example below will move the file 'code.py' to 'foldername'

{% highlight shell %}
$ mv code.py foldername/
{% endhighlight %}


## 4. man

This command is used to see the mannual of a particular command. On Linux and other Unix-like operating systems, man is the interface used to view the system's reference manuals.

**man** is the system's manual viewer; it can be used to display manual pages, scroll up and down, search for occurrences of specific text, and other useful functions.

{% highlight shell %}
$ man mkdir
{% endhighlight %}


## 5. mkdir

This make directory command is used to create a new directory in Linux.

{% highlight shell %}
$ mkdir foldername
{% endhighlight %}

## 6. rmdir

This remove directory command is used to remove an existing directory. This commands removes a directory only and only if the directory is empty.

{% highlight shell %}
$ rmdir foldername
{% endhighlight %}


## 7. touch

This command is used to make a file. Creates a empty file.

{% highlight shell %}
touch demo.py
{% endhighlight %}

The above command will create a empty file named demo.py

## 8. rm

The rm ("remove") command is used to delete files. When used recursively, it may be used to delete directories.
The most common used option with this command is -f and -r.

-f or --force deletes the file even if the file is write-protected and if rm can delete the file. 

-r you can use this option when you want to delete a folder and delete all the files/folder **recusively** present inside it.

{% highlight shell %}
$ rm file.cpp
$ rm -f demo.c
$ rm -r foldername
{% endhighlight %}


## 9. locate 

This command is used to find a file within the linux OS. If you don't know the exact name of the file then you can use wildcard character in your search keyword and locate a particular file.


The command will show the first 20 results i.e, the file that ends with .py
{% highlight shell %}
$ locate "*.py" -n 20
{% endhighlight %}

## 10. clear

This command is used to clear the terminal screen and wipes the board clean. For using the clear command we can simply type clear.

{% highlight shell %}
$ locate file.py
{% endhighlight %}


## 11. sudo

This is the command that you need whenever you want to execute a command that need root permission

{% highlight shell %}
$ sudo su
{% endhighlight %}



These are some of the commands that you can't live without when using linux specifically Ubuntu distro. To learn more about these commands you can use the man command as it shows the mannual of that particular command.

# Thanks.