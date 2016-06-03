---
layout: page
title: Remote Systems
subtitle: Connecting
minutes: 5
---

> ## Learning Objectives {.objectives}
>
> * Connect to a remote system using <code>ssh</code> command

Text about remote systems requires secure username/password setup prior to ssh 
working.

~~~ {.bash}
$ ssh spruce.hpc.wvu.edu -l training01
~~~

> ## Username Variation {.callout}
>
> In this lesson, we have used the username `training01`....
> text on how to know your username (both in training and normally)

~~~ {.output}
------------------------------------------------------------------------------
				   Welcome to the Spruce Knob Supercomputer
			Shared Research Facilities, West Virginia University
------------------------------------------------------------------------------
			  ** Unauthorized use/access is prohibited. **

The actual or attempted unauthorized access, use, or modification of this
system is strictly prohibited. Unauthorized users may be subject to
institutional disciplinary proceedings and/or criminal and civil penalties 
under
state, federal, or other applicable domestic and foreign laws. The use of this
system is monitored and recorded for administrative and security reasons.  
Anyone
accessing this system expressly consents to such monitoring and is advised that
if monitoring reveals possible evidence of criminal activity, the Institution
may provide the evidence of such activity to law enforcement officials.

In addition, users must ensure data that is protected by Federal
security or privacy laws (e.g., HIPAA, ITAR, FERPA, classified information, 
etc.)
is not stored on this system. This system is not intended to meet the enhanced
security required by those laws or regulations.

By logging on to this system, you acknowledge your awareness of and acceptance
of with WVU's Acceptable Use Policies and you agree not to store any of the
before mentioned protected data.

WVU Acceptable Use of Data and Technology Resources Policies:
http://it.wvu.edu/governance/standards-and-procedures/all-standards/au
------------------------------------------------------------------------------
~~~

~~~ {.output}
Password:
~~~

> ## Typed Password won't show {.callout}
>
> Some text about password won't echo

~~~ {.output}
______________________________________________________________________________

Questions and Problem Reports:
-  Email:     helpdesk@hpc.wvu.edu
-  Help Desk Ticket System:   https://helpdesk.hpc.wvu.edu

Additional information on Spruce Knob:
-  Documentation:  http://wiki.hpc.wvu.edu
-  HPC Website:    http://sharedresearchfacilities.wvu.edu/facilities/hpc
______________________________________________________________________________

Further system related information:

- Spruce Knob utilizes the TORQUE/PBS resource manager to manage compute
   resources.

	To run an interactive shell, issue:
		  qsub -I -q queue_name

	To submit a batch job, issue:       qsub job_script.sh
	To show all queued jobs, issue:     showq or qstat
	To check a job status:              checkjob <jobId>
	To kill a queued job, issue:        canceljob <jobId>

	Example PBS job scripts are located at:
	http://wiki.hpc.wvu.edu/hpc_wiki/index.php/Sample_Job_Scripts

	The following man pages provide helpful pbs information:
		man pbs_resources_linux (How-to request cluster resources)
		man qsub
		man qstat

- Spruce Knob utilizes Environment Modules to help manage different software
   packages available on the cluster.  "module avail" shows the available
   modules.

- Spruce has two file systems available to users:
   - $HOME (permanent storage that is backed up via snapshots, 10GB Limit)
   - $SCRATCH (temporary storage that is NOT backed up, current allocation 130 
     TB)

- Please acknowledge use of this Super Computing System (Spruce Knob) at WVU,
   which are funded in part by the National Science Foundation EPSCoR
   Research Infrastructure Improvement Cooperative Agreement #1003907, the
   state of West Virginia (WVEPSCoR via the Higher Education Policy Commission)
   and WVU, in your publications produced using these resources.
_
______________________________________________________________________________

Recent Updates:




----------------------------------User 
Quotas-----------------------------------
File Set      Usage (MB)    Limit (MB)    % Used    File Usage    Limit
----------  ------------  ------------  --------  ------------  -------
home                4624         10240        45          8691        0
scratch          4048755      62914560         6           826        0
group             880349      29360128         2           395        0
--------------------------------------------------------------------------------


[training01@srih0001 ~]$
~~~


If username matches to whoami output, can omit username with ssh command

~~~ {.bash}
$ whoami
~~~

~~~ {.output}
training01
~~~

~~~ {.bash}
$ ssh spruce.hpc.wvu.edu
~~~




