# DeploymentSQLiteError

I faced an issue when I did a deployment. The API server was working locally but stopped working on Azure Web App post deployment on endpoitns dependent on database. Non-database endpoints were working just fine.

This usually happens because the database is not ready or migrations are not ready or the db simply does not exist. 

Solutions

1. Try using an online SQL server. That way you can manage the migrations locally before deployment.
1. If you continue to use SQLite - the default option on the API server - then, upload the SQLite file with the migrations updated from local development, via Kudu. Just drag and drop.

# Hire Me

I work as a full time freelance software developer and coding tutor. Hire me at [UpWork](https://www.upwork.com/fl/vijayasimhabr) or [Fiverr](https://www.fiverr.com/jay_codeguy). 

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - [Jay's Developer Profile](https://jay-study-nildana.github.io/developerprofile)