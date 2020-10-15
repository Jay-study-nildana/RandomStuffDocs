# Database

I have added a note about the database choice. 

# SQLite shift in 0.2.X

Version 0.1.X (check VersionandChangeLog.md ), started off using an Azure SQL database, under a Azure SQL server. 

I almost always chose this option for the following reasons.

* I use multiple computers (at any given point of time, I maintain five developer computers spread across Windows and Mac), and having an online server gives the flexibility to access the same database everywhere. 
* Cloud hosted database has automatic database, recovery and security options. 

However, starting with 0.2.X (check VersionandChangeLog.md), I switched to using an SQLite database, which is bundled directly into the project itself. 

* The SQL server has the above mentioned conveniences. However, it is also an external dependency. For example, if a student of mine wishes to run the project, they will be forced to configure an SQL server to run the project. Now, the project runs out of the box.
* Cost savings - everything that runs on the cloud is paid for, even if I am using the cheapest developer plan with reduced workloads. This move saves some money for me.

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - https://thechalakas.com/