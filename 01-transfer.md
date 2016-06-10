---
layout: page
title: Remote Systems
subtitle: Transfer Files
minutes: 20
---

> ## Learning Objectives {.objectives}
>
> * Learn to transfer files from/to remote systems using <code>scp</code>


[Data Download](http://swcarpentry.github.io/shell-novice/shell-novice-data.zip)


Transfer a single file

~~~ {.bash}
$ scp notes.text spruce.hpc.wvu.edu:transfered.txt
~~~

> ## Hostname differences {.callout}
>
> We use spruce.hpc.wvu.edu, but any hostname you have login access to will 
> work.

~~~ {.output}
notes.txt                       100%   86     0.1KB/s   00:00
~~~


Transfer a directory

~~~ {.bash}
$ scp -r molecules spruce.hpc.wvu.edu:.
~~~

> ## '.' filename designation {.callout}
>
> Recall that '.' on the command-line is a shortcut for the current directory 
> when used in place of a file.  This will create a file with the same name on 
> the remote system in the default directory ($HOME).

~~~ {.output}
cubane.pdb                           100% 1158     1.1KB/s   00:00    
ethane.pdb                           100%  622     0.6KB/s   00:00    
methane.pdb                          100%  422     0.4KB/s   00:00    
octane.pdb                           100% 1828     1.8KB/s   00:00    
pentane.pdb                          100% 1226     1.2KB/s   00:00    
propane.pdb                          100%  825     0.8KB/s   00:00
~~~

A better way might be to copy the entire zip file

~~~ {.bash}
$ scp shell-novice.zip spruce.hpc.wvu.edu:
~~~

> ## No filename designation after the hostname {.callout}
>
> If you do not specify a filename after the hostname, scp will put the file(s) 
> with the same name on the local system in the default remote system location 
> ($HOME).  Hostname must end with ':' character.


We can check that the files are on the remote system

~~~ {.bash}
$ ssh spruce.hpc.wvu.edu ls
~~~
~~~ {.output}
molecules
shell-novice-data.zip
special.txt
~~~


> ## Command at the end of ssh {.callout}
>
> Placing a command at the end of an `ssh` command will make ssh execute that 
> command on the remote system, deliver the output, and then return back to the 
> local system.


Reverse the order of hostname and filename to download the file from the remote 
system.

~~~ {.bash}
$ scp mountaineer.hpc.wvu.edu:special.txt download.txt
$ ls
~~~
~~~ {.output}
download.txt
~~~


=======
> * Retrieve/put files from/to remote systems using <code>sftp</code>
> * Retrieve/put files from/to remote systems using <code>scp</code>

Connect using sftp

~~~ {.bash}
$ sftp spruce.hpc.wvu.edu
~~~

> ## Hostname difference {.callout}
>
> In this example we use `spruce.hpc.wvu.edu` as the hostname.  However, you 
> can use any hostname that you have login capabilities and ....
~~~

list remote directory

~~~ {.bash}
sftp> ls
~~~ 

list local directory

~~~ {.bash}
sftp> lls
~~~

change remote directory

~~~ {.bash}
sftp> cd
~~~ 

change local directory

~~~ {.bash}
sftp> lcd
~~~

download file

~~~ {.bash}
sftp> get
~~~

put file 

~~~ {.bash}
sftp> put
~~~

Use the -R flag for directories

~~~ {.bash}
sftp> put -R
~~~

sftp has a list of other commands mirror filesystem commands

~~~ {.bash}
sftp> help
~~~

exit sftp

~~~ {.bash}
sftp> exit
~~~

## Simplifying transfers with SCP

transfer a single file

~~~ {.bash}
$ scp localfile spruce.hpc.wvu.edu:remotefile
~~~

retrieve a file

~~~ {.bash}
$ scp spruce.hpc.wvu.edu:remotefile localfile
~~~

Use the -R flag for directories

~~~ {.bash}
$ scp -r spruce.hpc.wvu.edu:remotedir localdir
~~~
