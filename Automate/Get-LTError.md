---
schema: 2.0.0
---

# Get-LTError

## SYNOPSIS
This will pull the %ltsvcdir%\LTErrors.txt file into an object.

## SYNTAX

## DESCRIPTION

## EXAMPLES

### EXAMPLE 1
```powershell
PS C:\>Get-LTError | where {(Get-date $_.Time) -gt (get-date).AddHours(-24)}

Get a list of all errors in the last 24hr
```

### EXAMPLE 2
```powershell
PS C:\>Get-LTError | Out-Gridview

Open the log file in a sortable searchable window.
```

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

