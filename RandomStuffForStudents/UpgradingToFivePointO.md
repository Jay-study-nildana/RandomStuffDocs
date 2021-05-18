# UpgradingToFivePointO

Upgrading from old verion to 5.0

1. Update csproj

        <TargetFramework>net5.0</TargetFramework>
1. Delete bin and obj folders
1. clear the NuGet package cache.
        
        dotnet nuget locals --clear all
1. Upgrade all package version numbers in .csproj file to match dot net 5.0. The best way to do it is to search each package, one by one, at https://www.nuget.org, and then, put the number.
1. do a project restore to restore all packages.

        dotnet restore
1. Run the project and make sure everything is still spinning.


# References

1. https://docs.microsoft.com/en-us/aspnet/core/migration/31-to-50?view=aspnetcore-5.0&tabs=visual-studio-mac

# Hire Me

I work as a full time freelance software developer and coding tutor. Hire me at [UpWork](https://www.upwork.com/fl/vijayasimhabr) or [Fiverr](https://www.fiverr.com/jay_codeguy). 

# important note 

This code is provided as is without any warranties. It's primarily meant for my own personal use, and to make it easy for me share code with my students. Feel free to use this code as it pleases you.

I can be reached through my website - [Jay's Developer Profile](https://jay-study-nildana.github.io/developerprofile)