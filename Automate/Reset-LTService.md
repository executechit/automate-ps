# Reset-LTService
## SYNOPSIS
This function will remove local settings on the agent.
## SYNTAX
```powershell
Reset-LTService [-ID] [-Location] [-MAC] [-Force] [-NoWait] [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This function can remove some of the agents local settings.
ID, MAC, LocationID
The function will stop the services, make the change, then start the services.
Resetting all of these will force the agent to check in as a new agent.
If you have MAC filtering enabled it should check back in with the same ID.
This function is useful for duplicate agents.
## PARAMETERS
### -ID &lt;SwitchParameter&gt;
This will reset the AgentID of the computer
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -Location &lt;SwitchParameter&gt;
This will reset the LocationID of the computer
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       false
Accept wildcard characters  false
```
### -MAC &lt;SwitchParameter&gt;
This will reset the MAC of the computer
```
Required                    false
Position                    named
Default value                False
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
### -NoWait &lt;SwitchParameter&gt;
This will skip the ending health check for the reset process.

The function will exit once the values specified have been reset.
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
PS C:\>Reset-LTService

This resets the ID, MAC and LocationID on the agent.
```

### EXAMPLE 2
```powershell
PS C:\>Reset-LTService -ID

This resets only the ID of the agent.
```
