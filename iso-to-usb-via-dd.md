# ISO-TO-USB-VIA-DD
```
lsblk | grep "sda"
sudo umount /dev/sdaX
sudo dd if="/path/to/file.iso" of=/dev/sda bs=4M status=progress oflag=sync
sudo sync
```
