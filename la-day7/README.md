## Mount Options - Partitions

### Notes

* Review and lab this subject (TO-DO)
* Mount with UUID for precision on the partition used
* When using or planning a file system with ext4, make sure to enable the 64bit feature if it's intended to surpass the size of 16TB
* You should always secure swap file systems (chmod 0600) because it's a security breach if users can read on the swap file any root info
* Extra reading:
  * /etc/mke2fs.conf: https://linux.die.net/man/5/mke2fs.conf
  * https://helpdeskgeek.com/linux-tips/what-are-inodes-in-linux-and-how-are-they-used/
  * https://linuxhint.com/understanding_vm_swappiness/
  * https://www.kernel.org/doc/Documentation/sysctl/vm.txt
* Overall review: blocksize, inode

### Notable Commands

* dumpe2fs - dump ext2/ext3/ext4 filesystem information | prints the super block and blocks group information for the  filesystem present on device.
* blkid - locate/print block device attributes
* tune2fs - adjust tunable filesystem parameters on ext2/ext3/ext4 filesystems
* truncate - shrink or extend the size of a file to the specified size
* dd - convert and copy a file
* swapon, swapoff - enable/disable devices and files for paging and swapping

---

## Pseudo Filesystem /proc & /sys

### Notes

* Extra reading:
  * https://www.thegeekdiary.com/understanding-the-proc-file-system/
  * https://www.thegeekdiary.com/understanding-the-sysfs-file-system-in-linux/
* 

### Notable Commands
