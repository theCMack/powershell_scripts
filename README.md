# A Collection of PowerShell Scripts
Just some powershell scripts to do things.

- MapWindowsDiskstoVolumes.ps1
  - This will map the Windows Disks to the AWS VolumeIds
- ebsnvme-id.zip (ebsnvme-id.exe)
  - Will map nvme on Windows 2008 and newer
  - https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/nvme-ebs-volumes.html


### Run these remotely in PowerShell using Invoke-WebRequest like this

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
$ScriptFromGitHub = Invoke-WebRequest https://raw.githubusercontent.com/theCMack/powershell_scripts/master/MapWindowsDiskstoVolumes.ps1 -UseBasicParsing
Invoke-Expression $($ScriptFromGitHub.Content)
