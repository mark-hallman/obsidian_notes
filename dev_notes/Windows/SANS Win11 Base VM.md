
Removed Apps (deBloating)


### Apps Installed
See winget installs section below
VS Code
MS Terminal
PowerShell 7.4.3.0 (2024-07-22) - also set as default when starting terminal.
All Windows Updates applied

### Configuration Changes
1. SANS Desktop Image
2. Activate Windows with SANS product Key
3. WSL not installed
5. SystemInformer
6. Windirstat
7. sysinternals
8. Disable defneder (avast)
9. MS Terminal set as default terminal
10. MS Terminal set to open as admin 
11. VMware Tools 12.4.5
12. Added `C:\Program Files\VMware\VMware Tools` to path.
13. SANS EULA
14. Disabled 
	1. UAC
	2. Hyper-V
	3. Cred-Guard
	4.  Auto Windows Update

![[Pasted image 20240722112751.png]]

### winget installs

1. winget install voidtools.Everything
2. winget install Microsoft.PowerShell
3. winget install 7zip.7zip
4. winget install Microsoft.VisualStudioCode 
5. winget install voidtools.Everything winget 
6. install 7zip.7zip  
7. winget install Microsoft.VisualStudioCode  
8. winget install Mozilla.Firefox 
10. winget install Google.Chrome

### VM Cleanup
Cleanmgr+
CCleaner
sdelete
vmwareToolboxCmd.exe disk shrink
clear PowerShell history
compact disk outside VM from the VMware Workstation menu
