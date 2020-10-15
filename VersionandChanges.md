# Version and Changes

This is 0.2.0 aka ZeroPointTwoPointZero.

Full version log available at VersionandChangeLog.md.

# Version History and Change Log - 0.2.0

Also known as ZeroPointTwoPointZero in places where numbers are not allowed or string is preferable.

More details below.

# Major Changes - Project Wide

* Documentation - I always maintain extensive internal documention that is private for all my development projects. On a public repo update, I go ahead and include a readme with all neccessary details. This update to this repo adds a dedicated documentation folder.
* Versioning - Every commit and branch will include a dedicated versioning documentation. Apps and Api Server will utilize consistent version number.
* Authentication - API Server and the Apps now employ authentication using Auth0
* Authorization - API Server and the Apps now employ authorization by way of roles.
* GitHub Branches for versions - Version based branches on repository. For every major version upgrade, I plan to maintain a specific branch. It would make it easy to roll back in case of failures, and also provide insight into development of project over time.

# Major Changes - API Server

* xUnitTesting - Unit Testing via xUnit is now included in the API Server Project.
* Test Driven Development is now being followed for API Server development. That means, Dependency Injection coupled with industry standard interface usage.
* SQL Server to SQLite - Moved from an online SQL Server to a SQLite database. This makes the project more portable removing the requirement of having to configure a SQL server. (more details at  "SQLite shift in 0.2.X" in Database.md)
* Added /api/Admin/Hi
* Added /api/Moderator/Hi
* Added /api/Moderator/GetAllQuotes
* Added /api/TheOthers/claims
* Added /api/User/Hi
* Added ​/api​/User​/GetASpecificQuote

# Minor Changes - API Server 

* API EndPoint Re-organized - I have re-organized the APIs internally, so they fall into specific categories, making it easier to use. 
* /api/RandomQuotes/GetHoldOfthem moved to /api/UserNotLoggedIn/GetHoldOfthem
* /api/RandomQuotes/PutThemOn moved to /api/UserNotLoggedIn/PutThemOn
* /api/RandomStuffGeneratorAPIServerDetails/Hi moved to /api/ProjectDetails/Hi

# Bug Fixes - API Server

* no big fixes this time.

# Major Changes - React JS App

* App has been rebuilt from the ground up. Previous version app was a placeholder.
* Implements all endpoints introduced/upgraded in this version of the API Server
* Except this endpoint - /api/UserNotLoggedIn/PutThemOn
* Removed the theme dependency. Uses react strap bootstrap components, avoiding any possible licensing issues. I am not too worried about license but its good to not become married to the theme that was used in 0.1.X

# Minor Changes - React JS App 

* App has been rebuilt. every change is a major change.

# Bug Fixes - React JS App

* App is new. no bug fixes to report.

# Other Things

The initial version (lets call it 0.1.X) that was already deployed had essential things only. A foundational structure that did what it was supposed to do, put the foundation. 

This update is a major structural update for the entire project.