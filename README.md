# Docker Windows Process Isolation
> Install Docker in process isolation mode on Windows

## TL;DR:
### Docker Engine Community
- Requires [Docker Desktop for Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
- Requires Hyper-V
- Does not work if another hypervisor (e.g. VMWare) is active
- High overhead

### Docker Engine Enterprise
- No companion app
- Uses [Process Isolation](https://docs.microsoft.com/en-gb/archive/blogs/freddyk/process-isolation-for-containers-in-windows-10) as opposed to a VM (just like Linux)
- Works with another hypervisor
- Low overhead

This script will install the latter engine

## Support
Tested on `Windows 10 Pro 1909`. Should work on any Windows build `>1809`

## Installing
> WARNING :warning:: You are executing an online script with full administrator rights. Make sure you know what you are doing.

In an elevated (Administrator) PowerShell window, run:
```powershell
Invoke-Expression $((Invoke-WebRequest "https://raw.githubusercontent.com/ViRb3/docker-windows-containers/master/Install-Docker-Container.ps1").Content)
```

## Resources
Based on this [awesome article](https://github.com/ViRb3/docker-windows-process-isolation/blob/master/Install-Docker-Process-Isolation-Mode.ps1)