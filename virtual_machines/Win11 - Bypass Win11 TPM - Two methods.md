To bypass the Windows 11 TPM 2.0 requirement when installing on VMware Workstation or Fusion, you can modify the Windows 11 ISO or use registry hacks during the installation process. Here’s how you can achieve this:

### Method 1: Modify the Windows 11 ISO

1. **Download the Windows 11 ISO:**
    
    - Obtain the official Windows 11 ISO from Microsoft's website.
2. **Download and Install the Required Tools:**
    
    - You’ll need tools like `Rufus` and `oscdimg` (part of the Windows ADK).
3. **Modify the ISO using Rufus:**
    
    - Open `Rufus`.
    - Select the downloaded Windows 11 ISO.
    - In the `Image option` dropdown, select `Extended Windows 11 Installation (no TPM/no Secure Boot)`.
    - Create a bootable USB drive with this modified image.

### Method 2: Use Registry Hack During Installation

1. **Create a Windows 11 VM:**
    
    - Follow the standard steps to create a new virtual machine in VMware Workstation or Fusion.
2. **Start the Installation Process:**
    
    - Boot the VM from the Windows 11 ISO.
3. **Trigger Command Prompt:**
    
    - When you see the “This PC can’t run Windows 11” message, press `Shift + F10` to open the Command Prompt.
4. **Edit the Registry:**
    
    - In the Command Prompt, type `regedit` and press `Enter` to open the Registry Editor.
    - Navigate to `HKEY_LOCAL_MACHINE\SYSTEM\Setup`.
    - Right-click on `Setup`, select `New` > `Key`, and name it `LabConfig`.
    - Right-click on `LabConfig`, select `New` > `DWORD (32-bit) Value`.
        - Name it `BypassTPMCheck` and set its value to `1`.
        - Name it `BypassSecureBootCheck` and set its value to `1`.
        - Name it `BypassRAMCheck` and set its value to `1`.
5. **Close the Registry Editor and Command Prompt:**
    
    - Close the Registry Editor and then the Command Prompt.
    - Click the back button in the Windows setup screen and proceed with the installation again.

### Method 3: Add TPM to the VM Configuration

1. **Add TPM Device in VMware:**
    
    - **VMware Workstation:**
        - Power off the VM.
        - Go to `VM` > `Settings`.
        - Click `Add`, select `Trusted Platform Module`, and click `Finish`.
    - **VMware Fusion:**
        - Power off the VM.
        - Go to `Virtual Machine` > `Settings`.
        - Click `Add Device`, select `Trusted Platform Module`, and click `Add`.
2. **Ensure Secure Boot is Enabled:**
    
    - **VMware Workstation:**
        - In the VM settings, ensure that `Enable Secure Boot` is checked under the `Options` tab.
    - **VMware Fusion:**
        - In the VM settings, ensure that `Secure Boot` is enabled.

By following one of these methods, you can bypass the TPM 2.0 requirement and install Windows 11 on VMware Workstation or Fusion. Method 2 is often the most straightforward and doesn't require additional software or tools.