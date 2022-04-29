# MEM-Intune-WorkgroupSwitcher

![GitHub repo size](https://img.shields.io/github/repo-size/niklasrast/MEM-Intune-WorkgroupSwitcher)

![GitHub issues](https://img.shields.io/github/issues-raw/niklasrast/MEM-Intune-WorkgroupSwitcher)

![GitHub last commit](https://img.shields.io/github/last-commit/niklasrast/MEM-Intune-WorkgroupSwitcher)

This repository contains an script to change the default name from the workgroup on your windows client(s).

## Install:
```powershell
PowerShell.exe -ExecutionPolicy Bypass -Command .\INSTALL-Workgroup.ps1 -install
```

## Uninstall:
```powershell
PowerShell.exe -ExecutionPolicy Bypass -Command .\INSTALL-Workgroup.ps1 -uninstall
```

Change this line to update the Workgroup name on any client
```powershell
#Install Customer Workgroup
Add-Computer -WorkGroupName "MYWORKGROUPNAME"
```

After this change your client needs to be rebooted, what you can force from Microsoft Endpoint Manager.

### Parameter definitions:
- -install configures the schedule task to change the local admin passwords.
- -uninstall removes the schedule task and the script from the client.
 
## Logfiles:
The scripts create a logfile with the name of the .ps1 script in the folder C:\Windows\Logs.

## Requirements:
- PowerShell 5.0
- Windows 10 or later
- Azure Storage Account with Table

# Feature requests
If you have an idea for a new feature in this repo, send me an issue with the subject Feature request and write your suggestion in the text. I will then check the feature and implement it if necessary.

Created by @niklasrast 
