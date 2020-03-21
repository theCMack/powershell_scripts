# A Collection of PowerShell Scripts
Just some powershell scripts to do things.

- MapWindowsDiskstoVolumes.ps1
  - This will map the Windows Disks to the AWS VolumeIds 


### Run these remotely in PowerShell using Invoke-WebRequest like this

```powershell
$ScriptFromGitHub = Invoke-WebRequest https://github.com/theCMack/powershell_scripts/blob/master/MapWindowsDiskstoVolumes.ps1
Invoke-Expression $($ScriptFromGitHub.Content)
