---
layout: page
title: Remote Systems
subtitle: Transfer Files
minutes: 20
---

> ## Learning Objectives {.objectives}
>
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
