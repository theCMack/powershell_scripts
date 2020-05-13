# A Collection of PowerShell Scripts
Just some powershell scripts to do things.

- MapWindowsDiskstoVolumes.ps1
  - This will map the Windows Disks to the AWS VolumeIds 


### Run these remotely in PowerShell using Invoke-WebRequest like this

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
$ScriptFromGitHub = Invoke-WebRequest https://raw.githubusercontent.com/theCMack/powershell_scripts/master/MapWindowsDiskstoVolumes.ps1 -UseBasicParsing
Invoke-Expression $($ScriptFromGitHub.Content)
