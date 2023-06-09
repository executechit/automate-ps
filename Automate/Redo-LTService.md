# Redo-LTService
## SYNOPSIS
This function will reinstall the LabTech agent from the machine.
## SYNTAX
```powershell
Redo-LTService [[-Server] <String[]>] [[-ServerPassword] <String>] [[-LocationID] <String>] [-Backup] [-Hide] [[-Rename] <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This script will attempt to pull all current settings from machine and issue an 'Uninstall-LTService', 'Install-LTService' with gathered information.
If the function is unable to find the settings it will ask for needed parameters.
## PARAMETERS
### -Server &lt;String[]&gt;
This is the URL to your LabTech server.

Example: https://lt.domain.com

This is used to download the installation and removal utilities.

If no server is provided the uninstaller will use Get-LTServiceInfo to get the server address.

If it is unable to find LT currently installed it will try Get-LTServiceInfoBackup
```
Required                    false
Position                    1
Default value
Accept pipeline input       true (ByValue, ByPropertyName)
Accept wildcard characters  false
```
### -ServerPassword &lt;String&gt;
This is the server password that agents use to authenticate with the LabTech server.
```
SELECT SystemPassword FROM config;
```


```
Required                    false
Position                    2
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -LocationID &lt;String&gt;
The LocationID of the location that you want the agent in

example: 555
```
Required                    false
Position                    3
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -Backup &lt;SwitchParameter&gt;
This will run a New-LTServiceBackup command before uninstalling.
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -Hide &lt;SwitchParameter&gt;
Will remove from add-remove programs
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -Rename &lt;String&gt;
This will call Rename-LTAddRemove to rename the install in Add/Remove Programs
```
Required                    false
Position                    4
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -Force &lt;SwitchParameter&gt;
This will force operation on an agent detected as a probe.
```
Required                    false
Position                    named
Default value                False
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
PS C:\>Redo-LTService

This will ReInstall the LabTech agent using the server address in the registry.
```

### EXAMPLE 2
```powershell
PS C:\>Redo-LTService -Server https://lt.domain.com -Password sQWZzEDYKFFnTT0yP56vgA== -LocationID 42

This will ReInstall the LabTech agent using the provided server URL to download the installation files.
```
