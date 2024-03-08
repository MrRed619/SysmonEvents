In order to allow scipts to be run in powershell we first need to set the execution policy to allow our auditing scripts to be ran

Open Powershell and start with  
  
    Get-ExecutionPolicy  
    
to confirm the current execution policy. We can also Get-ExecutionPolicy -List

    Set-ExecutionPolicy RemoteSigned

Restricted — blocks any script file from running.

RemoteSigned — allows scripts to be created on the computer. However, scripts created on another device won’t run without a trusted signature.

AllSigned — allows all scripts to run. However, only if a trusted publisher has included a signature.

Unrestricted — runs any script without restrictions.

I tend to save my scripts in C:\Sysmon

    Import-Module C:\Sysmon\[Get-Event.psm1]

    Get-Module (to list all running modules)
