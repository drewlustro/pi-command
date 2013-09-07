# Pi Command

A collection of Raspberry Pi tasks and their related command line operations that I've come to use repeatedly (on Mac OS X whenever using a client machine).



### Restore Backup Image to SD Card

```bash
df -h # find the SD card's device identifier, like /dev/disk1s1
sudo diskutil unmount /dev/disk1s1 # unmount the SD card completely
sudo dd bs=1m if=/Users/yourname/rasp-pi-backup.img of=/dev/rdisk1 # perform the restore. using raw /dev/rdisk1 instead of /dev/disk1 makes for a faster restore
```

