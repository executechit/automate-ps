# Show-LTAddRemove
## SYNOPSIS
This function shows the LabTech install in the add/remove programs list.
## SYNTAX
```powershell
Show-LTAddRemove [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This function will rename the HiddenDisplayName registry key to show it in the add/remove programs list.
If there is not HiddenDisplayName key the function will import a new entry.
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
