## Discos e Partições

### Notes

* Recommended reading: 
  * https://www.maketecheasier.com/differences-between-mbr-and-gpt/
  * https://www.howtogeek.com/56958/htg-explains-how-uefi-will-replace-the-bios/


### Notable commands

* fdisk - manipulate disk partition table
* mkfs - build a Linux filesystem
* mkswap - set up a Linux swap area
* wipefs - wipe a signature from a device
* gdisk - Interactive GUID partition table (GPT) manipulator
* parted - a partition manipulation program
  * explore "help" and commands
* cfdisk - display or manipulate a disk partition table

## Planejamento de Partições

Considerando 1 TB de disco:

SO: Debian 10 / Ubuntu 20

* Desktop (option 1)
  - / - 20GB
  - /usr - 15GB
  - /var - 10GB (optional)
  - /home - 500GB
  - swap - 8gb (At least the same ammount of RAM in your machine, or 2x the amount of ram if your machine has low RAM)

* Desktop (option 2 - simplified)
  * / - 50GB
  * /home - 930GB
  * swap - 8gb

* E-mail server
  * / - 20GB
  * /var - 900GB (where the e-mails are usually stored)
  * /home - 5GB
  * swap - 16GB

* File Server
  * / - 20GB
  * /home - 5GB
  * /data - 900GB 
  * swap - 8 GB


* Web Server
  * / - 20GB
  * /home - 5GB
  * swap - 8 GB
  * /var - 950GB (possible to split the partition into two: /var/www and /var/log, /var is a simplified solution)
    * /var/www
    * /var/log

### Notes 

* Reasons use a well partitioned disk:
  * For security: use fine grained permissions to restrict operations to where they should be happening (e.g.: block operations from X applications to anywhere else other than /var)
  * Resiliency: problems that happen on one partition, will not affect adjacent ones. That way we reduce the surface area of the impact

## Partition Migration

### Notes

* Review this lesson with more attention, hands-on wasn't possible (previous setup is necessary)
* Recommended reading: 
  * https://www.howtogeek.com/howto/33552/htg-explains-which-linux-file-system-should-you-choose/
  * https://www.thegeekdiary.com/understanding-the-configuration-file-for-mounting-file-systems-etc-fstab/
  * 

### Notable commands

* mklost+found  - create a lost+found directory on a mounted Linux second extended file system
* 