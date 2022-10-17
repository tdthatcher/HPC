---
title: September 2022 Monthly Update
data: 2022-09-16
layout: default
brief: FY23 Allocation Process, FY23 System Time, External Access, Conda Jobs
---

# FY23 HPC Allocation Request Process Status

Please review this letter, provided  August 24, 2022 by email, to project teams which submitted an FY23 HPC allocation.

Dear HPC Users:

Many of you have been asking for updates on FY23 Eagle Allocations on Eagle and Kestrel.   NREL is working closely with EERE management on the allocations process, and we have a few updates.

Because the CPU portion of Kestrel is expected to be available mid-year, it is very likely that most projects will receive their requested computational time.   In many cases, EERE projects are likely to receive allocations in line with the request that allow projects to perform the best possible science, as given in the “Max” AU request.

Allocations this year will be split between Eagle and Kestrel.   Most of you indicated a minimum portion of your allocation to run on Eagle, and we will do our best to honor that request.  However, computational time on Eagle will remain a relatively scarce resource compared to time on Kestrel, meaning it is likely that large projects will receive more of their time on Kestrel compared to Eagle.

Because we have a large mid-year resource increase, you are likely to receive more of your allocation in Q3 and Q4 than you would in a normal year.   We recommend you keep in mind that you will have more computational resources available in Q3 and Q4 in project planning, and in setting milestones with the Department of Energy.   

Many of you have also asked about when decisions will be announced.   Because the Department of Energy tries to ensure allocation decisions take funding decisions into account, EERE final allocation decisions will be made in September.   Even if final decisions on allocations are delayed until after the start of FY23, funded projects should have access to Eagle, and the ability to run jobs, on October 1.

Please let me know if you have additional questions. 

Michael Martin
Pronouns: he/him/his
Staff Scientist | Computational Science Center

# Eagle System Maintenance Time

With the start of the new fiscal year of 2023, Eagle will be undergoing scheduled system maintenance beginning on October 1st, 2022, and will be unavailable for use while maintenance and repair work is completed. This outage may last through Friday, October 7th. Further details regarding this outage, including the length of time, work performed, and the status of other HPC systems that may be affected will be announced in the coming weeks via follow-up emails as details become available. Please be aware that all jobs from FY22 that are running at the changeover will be stopped, and no jobs will be able to be scheduled in FY22 that would cross into FY23.

# External Collaborator Access to Eagle

Due to recent changes in cybersecurity requirements, access to eagle.nrel.gov and eagle-dav.nrel.gov is changing for external (non-NREL) HPC users. External login nodes el4 and ed7 will be removed from the Science DMZ and replaced with a proxy host that will connect to the login nodes.


This change will take place during the October (FY23) system time. Internal NREL users will not be affected. Further details will be released once the change has been completed.


# Running Conda Jobs From Home Directories

There have been system slowdowns on Eagle recently due to users launching large jobs out of the /home filesystem, particularly jobs calling large conda environments. Please avoid launching large jobs from /home and consider moving your conda environments to your /projects directory before launching a multi-node job. The /home filesystem is not designed for the same high level of input/output operations that the Lustre-based /projects filesystem is built for. The slowdown that can result from a large job in /home can dramatically increase the job runtime, costing AU and possibly causing timeout failures, as well as impact other users and their jobs with system slowdowns, timeouts, and module loading errors.



