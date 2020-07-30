# PHP Connect Active Directory (AD)

## Goal: Use LDAP and PHP to authenticate with Active Directory

Many times in enterprise environments you already have an active directory server and all the users you would ever want to access something have an account there. So why go through the trouble of creating yet another authentication system? Why not just leverage those accounts, that way you eliminate another system to remember your password for, use your active directory system to enforce password strength, account lockouts, and all those other built in features that come with active directory.

Some notes about the implementation below: I implemented this on a windows 2012 server with IIS and PHP over FastCGI. Make sure that you have enabled / compiled the LDAP module in php. Where i defined the $adServer variable you can specify either the host name of the domain controller or the ip address. I also included a simple echo in the example to show you how to access objects of the active directory account logging in as well as a var dump so that you can see what the object contains. Please remove these once you know the information you are after.
