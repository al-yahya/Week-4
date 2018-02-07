# Week-4
week 4 upload
root@debian:/home/john# #!/bin/bash
root@debian:/home/john# #chpt3
root@debian:/home/john# echo "Identify permissions of a device"
Identify permissions of a device
root@debian:/home/john# ls -l
total 40
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Desktop
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Documents
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Downloads
-rwxr-xr-x 1 root root 12 Jan 31 14:43 hello_world
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Music
-rw-r--r-- 1 root root 1024 Jan 31 14:53 new_file
drwxr-xr-x 2 john john 4096 Nov 16 14:06 Pictures
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Public
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Templates
drwxr-xr-x 2 john john 4096 Aug 14 18:20 Videos
root@debian:/home/john# echo "find the path and attributes of devices"
find the path and attributes of devices
root@debian:/home/john# udevadm info --query=all --name=/dev/sda
P: /devices/pci0000:00/0000:00:0d.0/ata1/host0/target0:0:0/0:0:0:0/block/sda
N: sda
S: disk/by-id/ata-VBOX_HARDDISK_VB8d8895d0-e90ae51c
S: disk/by-path/pci-0000:00:0d.0-ata-1
E: DEVLINKS=/dev/disk/by-id/ata-VBOX_HARDDISK_VB8d8895d0-e90ae51c /dev/disk/by-path/pci-0000:00:0d.0-ata-1
E: DEVNAME=/dev/sda
E: DEVPATH=/devices/pci0000:00/0000:00:0d.0/ata1/host0/target0:0:0/0:0:0:0/block/sda
E: DEVTYPE=disk
E: ID_ATA=1
E: ID_ATA_FEATURE_SET_PM=1
E: ID_ATA_FEATURE_SET_PM_ENABLED=1
E: ID_ATA_SATA=1
E: ID_ATA_SATA_SIGNAL_RATE_GEN2=1
E: ID_ATA_WRITE_CACHE=1
E: ID_ATA_WRITE_CACHE_ENABLED=1
E: ID_BUS=ata
E: ID_MODEL=VBOX_HARDDISK
E: ID_MODEL_ENC=VBOX\x20HARDDISK\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20
E: ID_PART_TABLE_TYPE=dos
E: ID_PART_TABLE_UUID=aab588af
E: ID_PATH=pci-0000:00:0d.0-ata-1
E: ID_PATH_TAG=pci-0000_00_0d_0-ata-1
E: ID_REVISION=1.0
E: ID_SERIAL=VBOX_HARDDISK_VB8d8895d0-e90ae51c
E: ID_SERIAL_SHORT=VB8d8895d0-e90ae51c
E: ID_TYPE=disk
E: MAJOR=8
E: MINOR=0
E: SUBSYSTEM=block
E: TAGS=:systemd:
E: USEC_INITIALIZED=1795082

root@debian:/home/john# echo "use the dd device command"
use the dd device command
root@debian:/home/john# dd if=/dev/zero of=new_file bs=1024 count=1
1+0 records in
1+0 records out
1024 bytes (1.0 kB, 1.0 KiB) copied, 0.0012008 s, 853 kB/s
