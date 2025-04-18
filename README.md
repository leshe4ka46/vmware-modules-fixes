## fixes for vmware kernel modules at 6.14.2 kernel

```
cd /usr/lib/vmware/modules/source
sudo cp  vmnet.tar vmnet.tar.bak && sudo cp vmmon.tar vmmon.tar.bak
sudo tar -xvf vmnet.tar && sudo tar -xvf vmmon.tar
# edit

# archive and copile
sudo tar -cf vmnet.tar vmnet-only/ && sudo tar -cf vmmon.tar vmmon-only/
sudo vmware-modconfig --console --install-all 
```
