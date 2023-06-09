# Set-LTProxy
## SYNOPSIS
This function configures module functions to use the specified proxy
configuration for all operations as long as the module remains loaded.
## SYNTAX
```powershell
Set-LTProxy [[-ProxyServerURL] <String>] [[-ProxyUsername] <String>] [[-ProxyPassword] <String>] [-EncodedProxyUsername <String>] [-EncodedProxyPassword <String>] [-DetectProxy] [-ResetProxy] [-WhatIf] [-Confirm] [<CommonParameters>]
```
## DESCRIPTION
This function will set or clear Proxy settings needed for function and
agent operations. If an agent is already installed, this function will
set the ProxyUsername, ProxyPassword, and ProxyServerURL values for the
Agent.
NOTE: Agent Services will be restarted for changes (if found) to be applied.
## PARAMETERS
### -ProxyServerURL &lt;String&gt;
This is the URL and Port to assign as the ProxyServerURL for Module

operations during this session and for the Installed Agent (if present).

Example: Set-LTProxy -ProxyServerURL 'proxyhostname.fqdn.com'

Example: Set-LTProxy -ProxyServerURL 'proxyhostname.fqdn.com:8080'

This parameter may be used with the additional following parameters:

ProxyUsername, ProxyPassword, EncodedProxyUsername, EncodedProxyPassword
```
Required                    false
Position                    1
Default value
Accept pipeline input       true (ByValue, ByPropertyName)
Accept wildcard characters  false
```
### -ProxyUsername &lt;String&gt;
This is the plain text Username for Proxy operations.

Example: Set-LTProxy -ProxyServerURL 'proxyhostname.fqdn.com:8080' -ProxyUsername 'Test-User' -ProxyPassword 'SomeFancyPassword'
```
Required                    false
Position                    2
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -ProxyPassword &lt;String&gt;
This is the plain text Password for Proxy operations.
```
Required                    false
Position                    3
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -EncodedProxyUsername &lt;String&gt;
This is the encoded Username for Proxy operations. The parameter must be

encoded with the Agent Password. This Parameter will be decoded using the

Agent Password, and the decoded string will be configured.

NOTE: Reinstallation of the Agent will generate a new agent password.

Example: Set-LTProxy -ProxyServerURL 'proxyhostname.fqdn.com:8080' -EncodedProxyUsername '1GzhlerwMy0ElG9XNgiIkg==' -EncodedProxyPassword 'Duft4r7fekTp5YnQL9F0V9TbP7sKzm0n'
```
Required                    false
Position                    named
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -EncodedProxyPassword &lt;String&gt;
This is the encoded Password for Proxy operations. The parameter must be

encoded with the Agent Password. This Parameter will be decoded using the

Agent Password, and the decoded string will be configured.

NOTE: Reinstallation of the Agent will generate a new password.
```
Required                    false
Position                    named
Default value
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -DetectProxy &lt;SwitchParameter&gt;
This parameter attempts to automatically detect the system Proxy settings

for Module operations during this session. Discovered settings will be

assigned to the Installed Agent (if present).

Example: Set-LTProxy -DetectProxy

This parameter may not be used with other parameters.
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       true (ByPropertyName)
Accept wildcard characters  false
```
### -ResetProxy &lt;SwitchParameter&gt;
This parameter clears any currently defined Proxy Settings for Module

operations during this session. Discovered settings will be assigned

to the Installed Agent (if present).

Example: Set-LTProxy -ResetProxy

This parameter may not be used with other parameters.
```
Required                    false
Position                    named
Default value                False
Accept pipeline input       true (ByPropertyName)
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
