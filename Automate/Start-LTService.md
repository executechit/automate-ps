# Start-LTService
## SYNOPSIS
This function will start the LabTech Services.
## SYNTAX
```powershell
Start-LTService [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This function will verify that the LabTech services are present.
It will then check for any process that is using the LTTray port (Default 42000) and kill it.
Next it will start the services.
## PARAMETERS
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
