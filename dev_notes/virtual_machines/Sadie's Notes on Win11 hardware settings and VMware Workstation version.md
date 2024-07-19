
Link to SANS Confluence Page on QA concerns
https://sans-enterprise.atlassian.net/wiki/x/IwD8kgM


![[Screenshot 2024-07-18 at 1.18.50 PM.png]]

Hi Erik -1 know you're coming back from SANSFIRE meetings so I don't expect an immediate response and I hope that trip went well for you
Question: How do I update the sroc[.]io and faculty-facing Confluence pages that detail the VM/VMX requirements? We need to update them to reflect Windows 11VM requirements. Thank you in advance!
Erik Kristensen



![[Screenshot 2024-07-18 at 12.52.00 PM.png]]

hi Mike Pilkington
I've been keeping Mark posted on my testing. I've shared what I've done and also asked for some details on his build process. So I think we're already on the same page. And I just brought you up to speed too, so I don't think we'd solve much with another meeting. Ultimately, this comes down to what does SROC want to require? And I think that's more of an Erik K. decision. Historically, our VMware requirements have been the latest release minus 1. It would definitely make it simpler on SROC to change that requirement to simply students must have the latest version of VMware. But that's a bit of a political decision, because technically, we could continue to support latest release minus 1. At least that's what I've found in my testing. And in fact, the SEC401 VM proves that as well.


![[Screenshot 2024-07-18 at 12.52.17 PM.png]]

Sadie Gauthier 
Gotcha and thank you for letting me know. Mark and I have been discussing this since last week and those were the vague one requirement one strong suggestion that we came up with for now. What OS are you testing on? The reason for the 21 requirement was due to the fact that if a student comes in with a Win11machine then they will ***definitely have issues using a Win11 VM if they aren't on a more recent version of VMware AND if that setting isn't set to 21.***
Maybe you me and Mark can have a chat about it before it goes to Erik so we are all on the same/similar page?

Mike Pilkington
I've tested it on the following (again, my VM is using hardware version 18):
•	Windows 10 with Workstation 17.5.2
•	Windows 11 with VMware Workstation 16.2.4
•	macOS Monterrey with VMware Fusion 12.2.4
Also, I did a ton of development work for the SEC401 VM last year. That course VM was Windows 11 and I did it all on my Windows 11 host with VMware Workstation 16.2.4. It's HW version was also 18.

```
mh: All those combinations will run on 17.5.2.  17.5.2 can run hwv 21 and down to at least 18, probably lower.  

mh: Why did you pick 16.2 has the version to use?

mh: From VMware site: Workstation 16.2 is not compatible with Win11 host.

mh: Current laptop requirements on sans.org, shows that students with a Win11 host must use 17.5.2.  Wouldn't it be easier to just say 17.5.2 is required for all classes.  17.5.2 can run previously used standard of "18" and all  the way up to 21.  16.2.x can only 

```


![[Screenshot 2024-07-18 at 12.52.25 PM.png]]

hi Mike Pilkington 12:00pm
I've been keeping Mark posted on my testing. I've shared what I've done and also asked for some details on his build process. So I think we're already on the same page. And I just brought you up to speed too, ***so I don't think we'd solve much with another meeting***. Ultimately, this comes down to what does SROC want to require? And I think that's more of an Erik K. decision. ***Historically, our VMware requirements have been the latest release minus 1***. It would definitely make it simpler on SROC to change that requirement to simply students must have the latest version of VMware. But ***that's a bit of a political decision***, because technically, we could continue to support latest release minus 1. At least that's what I've found in my testing. And in fact, the SEC401 VM proves that as well.  

```
mh: On Mike's comment about 410 - So what about 710's Win11 VM that would not run with changing the virt.hw setting to 21?  This one reason that I'm concered with testing all the relevant versions of Workstation and Fusion. (at least two versions)

mh: Latest - 1 = 17.5.1 so they likely will have to upgrade so why not have the students to install the latest. All the tests and comments about 16.2 are moot because that version is already older than the current requirements allows.
```


Sadie:
lAwesome! Okay, then I think we should set up a call with you, myself, and Mark to discuss your findings as well as Mark's findings and see if we can get a better handle on this. Are you free this afternoon or tomorrow?

```
mh: Did Sadie mis the point that Mike said he didn't think that a meeting was required?  She asked him again about setting up a meeting.
```

