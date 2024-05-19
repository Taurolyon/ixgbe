== Patched ixgbe drivers for use with Proxmox 8 VE ==
Tested with 6.8.4-3-pve kernel, and configured to use DKMS for easier updates.

Original source from: https://psychz.dl.sourceforge.net/project/e1000/ixgbe%20stable/5.20.3/ixgbe-5.20.3.tar.gz

Credit to cybernard - https://forum.proxmox.com/threads/intel-x553-sfp-ixgbe-no-go-on-pve8.135129/post-661611

===Installation===
```
git clone https://github.com/Taurolyon/ixgbe.git

sudo apt install dkms gcc make proxmox-headers-$(uname -r)

sudo cp -R ./ixgbe-5.20.3 /usr/src/

sudo dkms add -m ixgbe -v 5.20.3

sudo dkms build -m ixgbe -v 5.20.3

sudo dkms install -m ixgbe -v 5.20.3

echo "ixgbe" | sudo tee -a /etc/modules
```

As long as you have no errors along the way, reboot, and you should have a working ixgbe driver!
