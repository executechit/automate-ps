# Uninstall-LTService
## SYNOPSIS
This function will uninstall the LabTech agent from the machine.
## SYNTAX
```powershell
Uninstall-LTService [[-Server] <String[]>] [-Backup] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This function will stop all the LabTech services. It will then download the current agent install MSI and issue an uninstall command.
It will then download and run Agent_Uninstall.exe from the LabTech server. It will then scrub any remaining file/registry/service data.
## PARAMETERS
### -Server &lt;String[]&gt;
This is the URL to your LabTech server.

Example: https://lt.domain.com

This is used to download the uninstall utilities.

If no server is provided the uninstaller will use Get-LTServiceInfo to get the server address.
```
Required                    false
Position                    1
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -Backup &lt;SwitchParameter&gt;
This will run a 'New-LTServiceBackup' before uninstalling.
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       true (ByPropertyName)
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
PS C:\>Uninstall-LTService

This will uninstall the LabTech agent using the server address in the registry.
```

### EXAMPLE 2
```powershell
PS C:\>Uninstall-LTService -Server 'https://lt.domain.com'

This will uninstall the LabTech agent using the provided server URL to download the uninstallers.
```
