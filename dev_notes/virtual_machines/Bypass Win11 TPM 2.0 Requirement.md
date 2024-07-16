**Clip source:** [How to bypass the Windows 11 TPM 2.0 requirement](https://www.bleepingcomputer.com/news/microsoft/how-to-bypass-the-windows-11-tpm-20-requirement/)

  

# How to bypass the Windows 11 TPM 2.0 requirement

By

###### **[Lawrence Abrams](https://www.bleepingcomputer.com/author/lawrence-abrams/)**

- July 2, 2021
    
- 11:22 AM
    
- [38](https://www.bleepingcomputer.com/news/microsoft/how-to-bypass-the-windows-11-tpm-20-requirement/#comments)
    

![](https://www.evernote.com/shard/s2/res/7bc409a6-25a7-42a8-941e-881bfc29a287)

Microsoft now requires a computer to have a TPM 2.0 module to install Windows 11. However, new Registry entries have been discovered that allow you to bypass the TPM requirement and minimum memory and secure boot requirements.

  

With Windows 11, Microsoft added new [minimum system requirements](https://www.bleepingcomputer.com/news/microsoft/microsoft-publishes-the-windows-11-system-requirements/) that all devices [need to have a TPM 2.0 security processor](https://www.bleepingcomputer.com/news/microsoft/windows-11-wont-work-without-a-tpm-what-you-need-to-know/) to power some of the operating system's security features.

  

"The following Windows features require TPM 2.0: Measured Boot, Device Encryption, WD System Guard, Device Health Attestation, Windows Hello/Hello for Business, TPM Platform Crypto Provider Key Storage, SecureBIO, DRTM, vTPM in Hyper-V," Microsoft told BleepingComputer.

  

1/100:00Skip Ad Continue watchingMicrosoft shares temp fix for Windows 11 Photos not launchingafter the adVisit Advertiser website[GO TO PAGE](https://www.bleepingcomputer.com/news/microsoft/how-to-bypass-the-windows-11-tpm-20-requirement/#) PLAY

![](https://www.evernote.com/shard/s2/res/2c4cc6d9-bef0-49b4-9433-9a7497657de2)

Latest Stories Video SettingsFull ScreenAbout ConnatixV509406

  

![](https://www.evernote.com/shard/s2/res/738c7d11-6b4e-4464-86b8-9d50ce695098)

[Read More](https://www.bleepingcomputer.com/news/security/new-bugsleep-malware-implant-deployed-in-muddywater-attacks/?traffic_source=Connatix "New BugSleep malware implant deployed in MuddyWater attacks")

  

![](https://www.evernote.com/shard/s2/res/3bfed6dc-38f0-4e70-b95c-1d43465e707b)

[Read More](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-temp-fix-for-windows-11-photos-not-launching/?traffic_source=Connatix "Microsoft shares temp fix for Windows 11 Photos not launching")

  

![](https://www.evernote.com/shard/s2/res/1be87863-40a5-4391-9cf9-d7c816936157)

[Read More](https://www.bleepingcomputer.com/news/security/sexi-ransomware-rebrands-to-apt-inc-continues-vmware-esxi-attacks/?traffic_source=Connatix "SEXi ransomware rebrands to APT INC, continues VMware ESXi attacks")[Read More](https://www.bleepingcomputer.com/news/microsoft/june-windows-server-updates-break-microsoft-365-defender-features/?traffic_source=Connatix "June Windows Server updates break Microsoft 365 Defender features")

  

![](https://www.evernote.com/shard/s2/res/8e7fdcff-caf0-4290-8f66-3510321ca6c9)

[Read More](https://www.bleepingcomputer.com/news/security/facebook-ads-for-windows-themes-push-sys01-info-stealing-malware/?traffic_source=Connatix "Facebook ads for Windows desktop themes push info-stealing malware")

  

![](https://www.evernote.com/shard/s2/res/c52ae3f1-9f81-4d0e-9ec1-5e2f3fb23911)

[Read More](https://www.bleepingcomputer.com/news/security/banks-in-singapore-to-phase-out-one-time-passwords-in-3-months/?traffic_source=Connatix "Banks in Singapore to phase out one-time passwords in 3 months") [New BugSleep malware implant deployed inMuddyWater attacks](https://www.bleepingcomputer.com/news/security/new-bugsleep-malware-implant-deployed-in-muddywater-attacks/?traffic_source=Connatix "New BugSleep malware implant deployed in MuddyWater attacks")

  

![](https://www.evernote.com/shard/s2/res/003bc0b9-d3a7-4aaf-8380-c3e9de56dcda)

For most people running CPUs created in the past 5-6 years, a firmware-based TPM (fTPM) is built into the CPU and can be enabled in the BIOS.

  

To enable the fTPM, simply boot your computer into the BIOS and enable the Intel Platform Trust Technology (Intel PTT) or the AMD Platform Security Processor, depending on your CPU.

  

For those who do not have this feature, you may be able to install a discrete TPM 2.0 processor on the motherboard. However, if your processor is old enough that it does not have one built-in fTPM, your motherboard's module will likely be TPM 1.2, which is not compatible with Windows 11.

  

This requirement is frustrating for users running Windows 10 on older equipment, as now they are being forced to purchase new hardware to install Windows 11.

  

Furthermore, as Microsoft has [stated in documentation](https://download.microsoft.com/download/7/8/8/788bf5ab-0751-4928-a22c-dffdc23c27f2/Minimum%20Hardware%20Requirements%20for%20Windows%2011.pdf) that OEMs can get permission to disable the TPM requirement in Windows 11 for their devices, the question becomes: Do you really need a TPM 2.0 processor to use Windows 11?

  

## **How to bypass the TPM requirement in Windows 11**

If you are attempting to install Windows 11 and receive a message stating, "This PC can't run Windows 11," it is likely that you do not have a TPM 2.0 installed or enabled.

  

The good news is that Microsoft includes a new 'LabConfig' registry key that allows you to configure settings to bypass the TPM 2.0, the 4GB memory, and Secure Boot requirements.

  

Based on the name of this registry key, it is likely used by Microsoft or OEMs to set up a "lab" environment to test the Windows 11 on older equipment or when testing new features.

  

To bypass the TPM 2.0 requirements when installing Windows 11, please follow these steps:

  

1. Install Windows 11 via an ISO or the Windows 11 Insider Program. While installing Windows 11, if your computer does not meet the hardware requirements, you will see a message stating, "This PC can't run Windows 11."
    
    ![](https://www.evernote.com/shard/s2/res/4c308720-77d4-420a-bbd2-3bc1a20f6343)
    
      
    
    **Windows 11 setup blocked due to missing hardware requirements**
    
2. When you see the above message, press **Shift+F10** on your keyboard at the same time to launch a command prompt.  At this command prompt, type **regedit** and press **enter** to launch the Windows Registry Editor.
    
    ![](https://www.evernote.com/shard/s2/res/55440ee1-3bbe-4b61-b978-e2a987c334bd)
    
      
    
    **Opening command prompt in Windows Setup**
    
3. When the Registry Editor opens, navigate to **HKEY_LOCAL_MACHINESYSTEMSetup**, right-click on the **Setup** key and select **New** > **Key**.
    
      
    
    When prompted to name the key, enter **LabConfig** and press **enter**.
    
      
    
    Now right-click on the **LabConfig** key and select **New** > **DWORD  (32-bit) value** and create a value named **BypassTPMCheck**,and set its data to **1**. Now create the **BypassRAMCheck** and **BypassSecureBootCheck** values and set their data to **1** as well, so it looks like the following image.
    
    ![](https://www.evernote.com/shard/s2/res/67ec590a-443a-4188-a5d3-e50cc260d20b)
    
      
    
    **Configuring the Registry to bypass hardware requirements**
    
4. Once you configure those three values under the LabConfig key, close the Registry Editor, and then type **exit** in the Command Prompt followed by **enter** to close the window.
    
5. You will now be back at the message stating that the PC can't run Windows 11. Click on the back button in the Windows Setup dialog, as shown below.
    
    ![](https://www.evernote.com/shard/s2/res/e66bfad8-024e-4b4a-8603-4ab290ed0849)
    
      
    
    **Press the back button in Windows setup**
    
6. You will now be back at the screen prompting you to select the version of Windows 11 you wish to install. You can now continue with the setup, and the hardware requirements will be bypassed, allowing you to install Windows 11.
    
    ![](https://www.evernote.com/shard/s2/res/b81c7d0d-842b-45df-a4c5-26a8c5fdb16e)
    
      
    
    **Hardware requirements are now bypassed**
    

It is important to note that disabling these features could affect the performance or stability of Windows 11, so be sure to only use them on a virtual machine or test box that are you are ok with working in an unsupported environment.

  

Furthermore, by disabling the TPM 2.0 requirement, you are effectively reducing the security in Windows 11.

  

Finally, running Windows 11 on anything less than 4GB will not be an optimal experience and is not recommended.

  

_H/T [Albacore](https://twitter.com/thebookisclosed)_

  

### Related Articles:

[Microsoft says bug causes Windows 10 apps to display Open With dialogs](https://www.bleepingcomputer.com/news/microsoft/microsoft-says-bug-causes-windows-10-apps-to-display-open-with-dialogs/)

  

[Windows 11 KB5040442 update released with 31 fixes, changes](https://www.bleepingcomputer.com/news/microsoft/windows-11-kb5040442-update-released-with-31-fixes-changes/)

  

[Notepad finally gets spellcheck, autocorrect for all Windows 11 users](https://www.bleepingcomputer.com/news/microsoft/notepad-finally-gets-spellcheck-autocorrect-for-all-windows-11-users/)

  

[Microsoft pulls Windows 11 KB5039302 update causing reboot loops](https://www.bleepingcomputer.com/news/microsoft/microsoft-pulls-june-windows-11-kb5039302-update-causing-repeated-restarts/)

  

[Microsoft resumes rollout of Windows 11 KB5039302 update for most users](https://www.bleepingcomputer.com/news/microsoft/microsoft-resumes-rollout-of-windows-11-kb5039302-update-for-most-users/)