# Roles

As of now, the project is envisioned to have three roles. Higher levels, as they go down the list.

* Non Logged In User - Can See Quotes. 
* User - User level quote operations. for example, save a quote as favorite for later viewing.
* Moderator - Can do CRUD operations on Quotes. However, changes dont reflect to the end user yet.
* Admin - All powers. Approve CRUD operations on Quotes. Manage Users. And, everything else. 

Auth0 provides a system to manage roles. Those will be reflected in the API Server. Further, each roles, cascades into the next level user. Moderator includes User level privileges. Admin, includes, Moderator level privileges. The above order decides who is on top of who.

Specific details about each user, available below. Roles cascade downwards. For example, All the way down is Admin, who is assumed to have the privilege of everybody above him. So, Admin has privilege of Non Logged In User, like, See a Random Quote.

Note - Each Role that is implemented, should have a Permission Item attached to it. The same Permission Item must be documented in the Permissions.md file.

# Non Logged In User

* Can Visit Website and see public content.
* See a Random Quote - PermissionItem1

# User

* See Profile Page - PermissionItem2
* Save a Specific Quote as favorite
* See more details about Quote that is displayed on Random Quote or from favorite list
* See Stats, such as, i dont know. 
* Flag a quote, by providing an optional reason.
* See messages from website.
* Last Logged In

# Moderator

* See All Quotes In The System - PermissionItem3
* See All Quotes In The System - Pending Approval
* See All Quotes In The System - Rejected
* Quote CRUD - new and existing
* See All Quotes In The System - Flagged

# Admin

* Approve Quotes that are pending 
* See All Users
* See User Details
* Change User Role
* Site Stats like...i dont know. - PermissionItem4

# Privilege Response

As of now, the idea is to return a default behavior. API Endpoints are designed with these limitations and features.

* If privilege is denied, based on role, 403 Forbidden is returned by default by the API Server. The client can display whatever message it wants.
* If privilege is allowed, API server will continue as per the endpoint response

Future

* Perhaps, we can include, specific responses. Right now, I must keep things simple.
* For instance, when a Moderator tries to Approve a quote, instead of a Forbidden, we could say, you need "Admin Privileges Required" instead of a standard 403 message. Of course, the clients can do this themselves. Unfortunately, the 403 can mean anything. Perhaps, we can include the neccessary message in the 403 response.

# Roles Management on Auth0

Auth0 has many ways to manage permission and roles. In this project, I have decided to do the following. 

* Permissions are linked to a specific scope.
* Roles have all the permissions required attached to them. 

The thing about roles having all the permissions is important because, Auth0 allows a single user to have multiple roles. That is actually convenient. However, I want to make to manage roles permissions on my own. So, the end result is, each User has "exactly" one role, and the permissions are decided by this one role.

# Roles Management on App Clients

Client apps must include scope information in their token request. For instance, here is how scope works, with a basic React JS app.

    {
        "HelloWorld":"Random Sentence put here for kicks",
        "domain": "randomquoteexperimental.us.auth0.com",
        "clientId": "aZ7ozbAV2Hi7WWkGsNwVRZoYb82xgNF6",
        "audience": "https://thechalakas.com",
        "scope":"read:current_user update:current_user_metadata read:capquotes read:penquotes"    
    }

Specifically, here.

    "scope":"read:current_user update:current_user_metadata read:capquotes read:penquotes"

Add neccessary, scopes aka permissions from the Auth0 dashboard. Ideally, you simply add every scope in the system, since, as of now, i have a single client app that is designed to work on roles. The Auth0 system will respond with only those permissions as per the role attached to the user. 

So, essentially, the user can request every scope, but only those authorized, will be returned.

# Testing Assistance

I have a Postman Collection ready to use. Collection name - RolesTestingOct10th2020.postman_collection.json.

# Other Limitations and Notes

* Right now, the whole system is based on the assumption that the "Authorize" attribute will limit access as per the access policies. If a system hacker, manages to go over this policy, there is nothing inside components can do about this.
* For example, take an interface that adds new quotes. It is possible to include a second level of gate. This second gate could check again, if the user has the specific role, to add new quote. However, I am not going to do that.

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - https://thechalakas.com/