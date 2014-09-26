# Office 365 scripts and utilities

Office 365 utilities, PowerShell scripts and related stuff.

## PowerShell scripts

#### Get-SPOInvalidFilesForSync
This script allows you to search for long paths on SharePoint Online document libraries that normally causing synchronization issues with OneDrive for Business 2013. The limitations and restrictions are described at http://support.microsoft.com/kb/2933738

**Requirements**: install SharePoint Server 2013 Client Components SDK: http://www.microsoft.com/en-ie/download/details.aspx?id=35585

**Syntax**
```
.\Get-SPOInvalidFilesForSync.ps1 -SiteName "https://mytenant.sharepoint.com" 
                                 -DocumentLibraryName "My Documents" 
                                 -Credential $credentials 
                                 -Verbose
```

*-SiteName*              The SharePoint Online site's URL. Ensure to specify https

*-DocumentLibraryName*   Optional. The name of the library to process

*-Credential*            Optional. The credentials to be used to connect to SharePoint Online. If omitted, the script will pop up for input

*-Verbose*               Optional. If specified, all verbose messages will be shown
