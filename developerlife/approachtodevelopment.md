# Approach To Project Development

It always start with an idea. For instance, here, is a situation, that is happening with the random stuff project, as I type.

I was figuring out how to display all the quotes in a view. Further, I also wanted to show each quote in a separate box or something. I managed to get all the quotes shown in a view. Further, I was able to add a simple button to the list item. So, when I click on the button, the button knows, which quote is being interacted with. 

At this, (as obvious as it might sound), I realized, that I have not reached a point where I needed to access a specific Quote. This is the first step. 

# Step One - Feature Idea

A feature idea could be anything. right now, it is being able to see a specific quote. Another instance, this idea to build an entire product - Random Quote Generator - was a step one until I started this project. 

So, I have got a new feature idea (even if it sounds obvious, as mentioned before). What next? 

# Step Two - Decide on all things needed. 

Ultimately, everything has to start with an API endpoint. 

# Step Three - Design the API EndPoint 

This is where I sit and design the API Endpoint. This is not where I do the actual coding. I think in my head, or write it down in my work diary. 

Here, I design the main things. First, I need to answer the simple question. 

* is it getting things directly? 
* is it getting things after getting something from the client?
* is it just receiving things. 

In my case, it would be, getting things from the client - the quote id. Then, responding, which is returning the quote that was requested by the client. 

please note - client, here, means, the client app.

Now, I have decided the following.

* It is going to be POST call, and there will be a response. 
* It will be authorized POST call as only authorized folks can ask for a specific quote. 
* It will have a body, which contains details about the specific quote they are asking for. As of now, to identify a quote, all i need is a Quote ID. In fact, right now, and for the current future, Quote ID will be the only way to identify and get a specific quote. 
* I will need to return essential Quote Information. 

# Step Sideways Future Idea trigger

Okay, now, just as I was writing this plan, I got another idea. 

So, I already am returning a collection of Quotes. I could have different type of quote returns.

* I could have a basic quote return. Similar to what I am alreadying doing in the full Quote List Collection.
* I could have a full on detailed quote return. This might be useful for the roles I have in my project. In fact, the quote return should be decided by the role that is calling. Perhaps, the Quote Return should have multiple endpoints, for different users, based on their role, permissions and scope. 

So, Once, again, I go through all the steps, I am writing in this page, from start, about this whole Quote Return thing. 

# Step Five - Coding Begins

At this point, the design is locked in. Now, we begin the coding. 

* We are following TDD approach in this project. In order to make this happen, we must always start with an interface. 
* We start by writing the interfaces and the corresponding unit tests. 
* Once they pass, then begins the actual development of endpoint.
* I have a habit of using helper functions. I build the neccessary helper functions, which will then be used in the interface implementations used by the API EndPoint that is being built right now. 
* Once the API returns the neccessary type of Quote, we are most done with coding.
* In coding phase, interface implementations and helpers is where we run into challenges. This is where we apply the logic that solves the problem at hand. 
* I might be using some advanced queries, design patterns, libraries and so on. If something is new or complicated, I have a separate coding repository where I practice the neccessary things. 
* Once the practice project gives the desired results, bring that solved component into the main project
* NEVER DIRECTLY PRACTICE IN YOUR LIVE PROJECT. IT IS NOT COOL.

# Step Six - API EndPoint Testing

* API testing is complex, but right now, I am only concerned that it works. Not worried about speed or performance (that should and will come later)
* I usually use the built in Swagger documentation to do the testing. 
* I test it directly in the browser or use CURL. 
* If it is really essentially, Postman, is also not a bad idea. 

# Step Seven - Client Usage

* Now that the API is working, its time to use it in the client app. 
* As it is with API Coding, I usually have a separate coding repository where I practice. For every new API, I use the practice client app to get the API working, try out different UI elements, look and feel and so on. 
* Once I feel, its all good, move it over to the main project. Integrate the working code, so to speak. 

# Deployment 

* At this point of development, the project is already setup with CICD. 
* So, once I add the code to the API Server and the APP, the code should already be built and deployed to the live/production/site test as required.
* This is another reason why I dont like practising directly on the live code. The practice repository is not linked to the main repository, so there wont be any ten thousand builds triggre every time i take a break, and commit the code to the main repository. 
* There are other ways of dealing with this - use a different branch - so, my approach is one way to solve this situation.

# Other Notes

* In most cases, it is essential, you use a project management tool to do all this. 
* I usually open a Trell Card for each new idea implementation (and linking to new cards, as new ideas get generated) with all the above steps ready to roll.
* As the development (not just the code, but the whole sequence above) continues, steps get added, are performed, and ticked off as they are completed. 
* You could have a Trello Card Template, and create copies of it for every idea, to maintain consistency.


# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - [Jay's Developer Profile](https://jay-study-nildana.github.io/developerprofile)