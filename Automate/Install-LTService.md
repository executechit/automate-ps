---
schema: 2.0.0
---

# Install-LTService

## SYNOPSIS
This function will install the LabTech agent on the machine.

## SYNTAX

```
Install-LTService [-Server] <String[]> [-ServerPassword] <String> [[-LocationID] <Int32>] [[-TrayPort] <Int32>]
 [[-Rename] <String>] [-Hide] [-SkipDotNet] [-Force] [-NoWait] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
This function will install the LabTech agent on the machine with the specified server/password/location.

## EXAMPLES

### EXAMPLE 1
```powershell
PS C:\>Install-LTService -Server https://lt.domain.com -Password 'plain text pass' -LocationID 42

This will install the LabTech agent using the provided Server URL, Password, and LocationID.
```

## PARAMETERS

### -Server
This is the URL to your LabTech server.
example: https://lt.domain.com
This is used to download the installation files.
(Get-LTServiceInfo|Select-Object -Expand 'Server Address' -ErrorAction SilentlyContinue)

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerPassword
This is the server password that agents use to authenticate with the LabTech server.
```
SELECT SystemPassword FROM config;
```

```yaml
Type: String
Parameter Sets: (All)
Aliases: Password

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocationID
This is the LocationID of the location that the agent will be put into.
(Get-LTServiceInfo).LocationID

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 0
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TrayPort
This is the port LTSvc.exe listens on for communication with LTTray processes.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 0
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rename
This will call Rename-LTAddRemove after the install.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hide
This will call Hide-LTAddRemove after the install.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipDotNet
This will disable the error checking for the .NET 3.5 and .NET 2.0 frameworks during the install process.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
This will disable some of the error checking on the install process.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
This will skip the ending health check for the install process.
The function will exit once the installer has completed.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs. The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS