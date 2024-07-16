
  

`echo "shrink all drives:"`

`for shrinkpart in $( vmware-toolbox-cmd disk list ); do`

`vmware-toolbox-cmd disk shrink ${shrinkpart}`

`done`

Translated that to (The is run inside the VM)

**Linux VM**

`sudo vmware-toolbox-cmd disk shrink /`

**`Windows VM** - From Admin PS or CMD`

`vmwareToolboxCmd.exe disk shrink c:\`\

**The outside the VM**

`vmware-vdiskmanager -d <.VMDK file> # defrag`

`vmware-vdiskmanager -k <.VMDK file> # compact`