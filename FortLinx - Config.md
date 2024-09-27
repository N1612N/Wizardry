# Kali - FortLinx

---
#### Machine Information
```
Domain: FortKnox
Hostname:FortLinx
User: Coconut FortLinx
username: coconut
Password: linx
```

---
#### Packages 
- [x] Obsidian
- [x] Seclists
- [ ] Caido

---
#### System Logs
```
Enabled Shared folder and created a system link to shared folder in home directory
Sourced TMux Conf
Added Desktop Wallpaper and Disabled screenlock
```

---
#### Shell Scripts
###### VMWare Folder sharing and Linking to Home Directory
```sh
Enable the folder sharing in the VMWare Settings
sudo echo "# VMWare shared folder settings" >> /etc/fstab
sudo echo "vmhgfs-fuse /mnt/hgfs fuse defaults,allow_other 0 0" >> /etc/fstab
sudo reboot now
cd /mnt/hgfs
ln -s /mnt/hgfs/<VMShare> /home/<coconut/VMShare>
```


