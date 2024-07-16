
Slack message to Mike 

Good news / bad news

**Good news:** I was able to use the process described in article you gave me to create a VM without all the TPM encryption.  I added the three Registry entries after figuring out how to pause the install and drop to a command prompt with a Mac keyboard RPDing to a Windows machine. I removed these settings after the install was completed:

1. encryptedVM.guid  
2. encryption.data   
3. encryption.keySafe
4. vtpm.ekCRT        
5. vtpm.ekCSR        
6. vtpm.present      

The VM boots after following the process.

**Bad New**s - The VM is running extremely slow.  10+ seconds to launch Edge after clicking the icon.  The cursor disappears and will come back a few seconds later. At times it is basically unusable.   I tested other Win11 VMs (tpm turned on) on the same host and they are all running very slow.  I copies the VM to my mac mini and it runs slow there too.  so I not sure what that tells me except that it is probably not the host.

Looking at the task manager, Edge and Defender (antimalware service executable).  CPU is averaging over 70%. Maybe those process are doing some config or scans and performance will increase one they are done.  I going to leave them running for an hour or so and see if things improve. Running with Fusion,  performance is better but not great. My Windows machine is much more powerful that mac mini.

I have two more work arounds to test.  Although this approach works,  if we have to run the same process for each VM, it is going to be a PIA.  If was build a very basic Win11 VM that has the encryption removed,  it would be a much faster process.  

How are we going to do this Packer since part of the process is pause the install, drop to a command prompt, add the Registry entries, continue the Packer build.  This would be an issue with the Packer ISO build.  The VMX build, which uses an existing VM as a starting point should not have any issues.