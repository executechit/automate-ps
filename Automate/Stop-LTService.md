# Stop-LTService
## SYNOPSIS
This function will stop the LabTech Services.
## SYNTAX
```powershell
Stop-LTService [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This function will verify that the LabTech services are present then attempt to stop them.
It will then check for any remaining LabTech processes and kill them.
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
