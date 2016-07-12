---
layout: page
title: Working with Remote Systems
---


The source of power for the Unix shell comes from the available commands on the 
system you are working on.  Most systems which run Linux/Unix have very similar 
toolset (i.e. `grep`, `find`, `sort`).  However, there are specialized systems 
that are built to provide users with tremendous power.  Examples of these 
specialized systems include High Performance systems (HPC), visualization 
servers, and cloud computing.  All of these services have a connecting 
bottleneck, in that you need to remotely connect to them through network tools.  


The two lessons here are short and sweet.  They show the most common methods 
used to connect to remote systems, and transfer/retrieve files remotely.

> ## Prerequisites {.prereq}
>
> This lesson assumes basic understanding of the Unix shell and file systems.  
> You should be comfortable with moving around a file system using the shell 
> and running command-line programs.  Additionally, we assume that particpants 
> are using a command-line terminal, which can include MobaXterm or Cygwin 
> (Windows), or the associated Terminal emulator (Mac OS X or Unix/Linux).  If 
> you believe you need additional training on these topics you should check out 
> the [shell novice](https://swcarpentry.github.io/shell-novice) lesson first.
>
> If you are already comfortable with connecting to remote systems using ssh, 
> and/or transfering/retrieving files using scp/sftp, you probably won't learn 
> much from this lesson.

> ## Getting ready {.getready}
>
> Some of the examples in this lesson use specific files in their commands.  
> While any file or directory can be substituted for these files, if you would 
> like to execute the commands exactly you need to download the files we use 
> for this lesson.
>
> 1. Download [shell-novice-data.zip](shell-novice-data.zip).
> 2. Unzip/extract the file.  You should end up with a folder called 
>    data-shell.


## Topics

1. [Connecting to Remote Systems](00-connect.html)
2. [Transfering Files](01-transfer.html)


