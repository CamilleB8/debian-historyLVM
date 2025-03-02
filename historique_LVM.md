- lsblk
- pvcreate /dev/sdb
- vgextend debian-vg /dev/sdb
- vgdisplay debian-vg
- lvcreate -L 1G -s -n home-snap /dev/debian-vg/home
- lvextend -L +100%FREE /dev/debian-vg/home
- lvextend -l +100%FREE /dev/debian-vg/home
- mkdir /home-snap
- mount /dev/debian-vg/home-snap /home-snap
- ls /home-snap
- touch /home-snap/test.txt
- ls /home-snap
- unmont /home-snap
- umont /home-snap
- umount /home-snap
- lvremove /dev/debian-vg/home-snap
- lvs
- cat ~/.bash_history > historique_LVM.txt

![image](https://github.com/user-attachments/assets/ec6c7de1-5c58-44f5-9b84-b912ceb16fb2)
![image](https://github.com/user-attachments/assets/20946b42-3e0a-4177-8564-5ec60f1c98b8)
