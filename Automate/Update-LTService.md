# Update-LTService
## SYNOPSIS
This function will manually update the LabTech agent to the requested version.
## SYNTAX
```powershell
Update-LTService [[-Version] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This script will attempt to pull current server settings from machine, then download and run the agent updater.
## PARAMETERS
### -Version &lt;String&gt;
This is the agent version to install.

Example: 120.240

This is needed to download the update file. If omitted, the version advertised by the server will be used.
```
Required                    false
Position                    1
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -WhatIf &lt;SwitchParameter&gt;

```
Required                    false
Position                    named
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -Confirm &lt;SwitchParameter&gt;

```
Required                    false
Position                    named
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
## EXAMPLES
### EXAMPLE 1
```powershell
PS C:\>Update-LTService -Version 120.240

This will update the Automate agent to the specific version requested, using the server address in the registry.
```

### EXAMPLE 2
```powershell
PS C:\>Update-LTService

This will update the Automate agent to the current version advertised, using the server address in the registry.
```
