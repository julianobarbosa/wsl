# wsl
Windows Subsystem Linux

Installation Instructions for WSL 2

    05/29/2019
    2 minutes to read
    Contributors
        mscraigloewen 

To install and start using WSL 2 complete the following steps:

    Enable the 'Virtual Machine Platform' optional component
    Set a distro to be backed by WSL 2 using the command line
    Verify what versions of WSL your distros are using

Please note that you'll need to be running Windows 10 build 18917 or higher to use WSL 2, and that you will need to have WSL already installed (you can find instructions to do so here).
Enable the 'Virtual Machine Platform' optional component

Open PowerShell as an Administrator and run:
```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

After these changes are enabled you will need to restart your computer.
Set a distro to be backed by WSL 2 using the command line

In PowerShell run:
```powershell
wsl --set-version <Distro> 2
```

and make sure to replace <Distro> with the actual name of your distro. (You can find these with the command: wsl -l). You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.

Additionally, if you want to make WSL 2 your default architecture you can do so with this command:
```powershell
wsl --set-default-version 2
```

This will make any new distro that you install be initialized as a WSL 2 distro.
Finish with verifying what versions of WSL your distro are using

To verify what versions of WSL each distro is using use the following command:
```powershell
wsl --list --verbose or wsl -l -v
```
The distro that you've chosen above should now display a '2' under the 'version' column. Now that you're finished feel free to start using your WSL 2 distro!

# Reference
## [WSL2](https://docs.microsoft.com/en-us/windows/wsl/wsl2-install)
## [GITHUB] (https://github.com/microsoft/WSL/issues)
#
