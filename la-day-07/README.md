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
  * https://man7.org/linux/man-pages/man5/proc.5.html
  * https://man7.org/linux/man-pages/man5/sysfs.5.html
* Whenever possible, read files directly from /proc/ (e.g.: cat /proc/mounts instead of mounts) for increased performance whenever you avoid the execution of another binary
* 

### Notable Commands

* tset, reset - terminal initialization

---

## Discard and Trimming

### Notes

* Whenever you have a SSD, it is interesting to configure the Discard feature on the disk, to sync the inodes whenever there are removed or updated blocks
  * Important to consider, the discard feature might also negatively impact your performance, so consider running the fstrim command periodicaly

### Notable Commands

* fstrim - discard unused blocks on a mounted filesystem

--- 

## Other File systems

### Notes

* Extra reading
  * https://opensource.com/article/18/4/ext4-filesystem
  * https://www.diskinternals.com/glossary/reiserfs/

---

## LVM - Logical Volume Manager

### Notes

* Extra reading:
  * https://wiki.debian.org/LVM
  * https://tldp.org/HOWTO/LVM-HOWTO/
  * https://unix.stackexchange.com/questions/60091/where-is-the-documentation-for-what-sda-sdb-dm-0-dm-1-mean
* When using lvm, always use the least amount of space required for the application to run, because increasing the storage is easy and can be done while the machine is being used, but decreasing it might be troublesome and require interruptions
* TO-DO: Retake the quiz!

### Notable Commands

* lvm — LVM2 tools: The Logical Volume Manager (LVM) provides tools to create virtual block devices from physical devices.
  * pvcreate - Initialize physical volume(s) for use by LVM
  * pvdisplay - Display various attributes of physical volume(s)
  * pvs - Display information about physical volumes
  * vgcreate - Create a volume group
  * vgdisplay - Display volume group information
  * vgs - Display information about volume groups
  * lvcreate - Create a logical volume [e.g.: ]
  * lvdisplay - Display information about a logical volume
  * lvs - Display information about logical volumes
  * lvextend - Add space to a logical volume
* resize2fs - ext2/ext3/ext4 file system resizer
* partprobe - inform the OS of partition table changes
* lsblk - list block devices
