# Random Stuff Generator - The Idea

The idea is here is that, I am the owner of a company, that delivers quotes over the internet. Somehow, by magic, people are paying for it, also, by some magic!

I start by thinking of the consumer. I have three consumers for my company.

* Quote Reader - the final customer who likes to read a quote, as required.
* Quote Moderator - An internal customer who is responsible for managing the quotes and content
* Quote Admin - An internal customer who is responsible for all the admin tasks like user management, role management with access to every data that is available to make a better decision to build and run the business profitably.

# App - Front End

A single app is available that serves all three customers. Depending on their login, to which they are attached roles, the app will change giving them appropriate options. 

# API Server - Back End

The API Server serves the information as required by the user. Some of the things that are done here. 

* Provides Authentication - Users can login using a login method of their choice. 
* Provides Authorization - Users have roles attached to them. The App makes available different views based on these roles.
* Serves Quotes - The primary purpose of the product. The API Server, serves quotes.
* Serves Admin Data - All the information related to business like users, statistics, service health and everything else that a admin needs

# Infrastructure - DevOps

Every code that is part of backend and front end, is designed to work with continuos integration and continuous deployment, aka, CICD. As and when I fix bugs, add new features, they become immediatly available to the end user. 

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - https://thechalakas.com/