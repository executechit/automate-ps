# New-LTServiceBackup
## SYNOPSIS
This function will backup all the reg keys to 'HKLM\SOFTWARE\LabTechBackup'
This will also backup those files to "$((Get-LTServiceInfo).BasePath)Backup"
## SYNTAX
```powershell
New-LTServiceBackup [<CommonParameters>]
```
