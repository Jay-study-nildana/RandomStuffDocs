# Adding New Scopes

The API Server is already configured to work with Permissions, Scopes and Roles. This page is about how to add new scopes to the API Server.

Note : If you want to know how to configure scopes to the API server, check workdiaryExperimental.md and the official documentation of Auth0.

# Step 1

Add the new scopes here.

    services.AddAuthorization(options =>
    {
        //TODO1 - similar to above , migrate this also to appsettings.json
        //these are some test roles. 
        options.AddPolicy("capquotes", policy => policy.Requirements.Add(new HasScopeRequirement("read:capquotes", "https://randomquoteexperimental.us.auth0.com/")));
        options.AddPolicy("penquotes", policy => policy.Requirements.Add(new HasScopeRequirement("read:penquotes", "https://randomquoteexperimental.us.auth0.com/")));
        //Check Roles.md for detailed documentation on how roles are defined in this project
        //policy related to User Role
        options.AddPolicy("User", policy => 
        {
            policy.Requirements.Add(new HasScopeRequirement("read:profiledetails", "https://randomquoteexperimental.us.auth0.com/"));
        });
        //policy related to Moderator Role
        options.AddPolicy("Moderator", policy =>
        {
            policy.Requirements.Add(new HasScopeRequirement("read:profiledetails", "https://randomquoteexperimental.us.auth0.com/"));
            policy.Requirements.Add(new HasScopeRequirement("read:seeallquotes", "https://randomquoteexperimental.us.auth0.com/"));
        });
        //policy related to Admin Role
        options.AddPolicy("Admin", policy =>
        {
            policy.Requirements.Add(new HasScopeRequirement("read:profiledetails", "https://randomquoteexperimental.us.auth0.com/"));
            policy.Requirements.Add(new HasScopeRequirement("read:seeallquotes", "https://randomquoteexperimental.us.auth0.com/"));
            policy.Requirements.Add(new HasScopeRequirement("read:sitestats", "https://randomquoteexperimental.us.auth0.com/"));
        });
    });

# Step 2

Then, use them, in a controller or action like this.

        [Authorize(Policy = "capquotes")]

# Useful Links

* https://docs.microsoft.com/en-us/aspnet/core/security/authorization/policies?view=aspnetcore-3.1
* https://docs.microsoft.com/en-us/dotnet/api/microsoft.aspnetcore.authorization.authorizationoptions?view=aspnetcore-3.1
* Check Roles.md to see how I have designed Roles, Permissions and scopes, in this project.

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - https://thechalakas.com/