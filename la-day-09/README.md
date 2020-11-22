## User administration && Adding users

### Notes

* check /etc/adduser.conf for the default adduser configuration
* check syntax for useradd and adduser
* Extra reading:
  * https://www.computernetworkingnotes.com/rhce-study-guide/etc-passwd-file-in-linux-explained-with-examples.html
  * https://www.2daygeek.com/understanding-linux-etc-shadow-file-format/#:~:text=The%20%2Fetc%2Fshadow%20file%20stores,less%20of%20a%20security%20risk.
  * https://www.cyberciti.biz/faq/understanding-etcgroup-file/
  * https://man7.org/linux/man-pages/man1/passwd.1.html
  * https://linux.die.net/man/1/gpasswd
* /etc/passwd for user info, and /etc/shadow for password info
* /etc/group for group info,o and /etc/gshadow for group password info
* adding a password to a group, makes the user type in the password to be able to join(newgrp), and the user can only join temporarily (one session)
* 

### Notable Commands

* adduser, addgroup - add a user or group to the system
* useradd - create a new user or update default new user information
* deluser, delgroup - remove a user or group from the system
* userdel - delete a user account and related files
* groupadd - create a new group
* groupdel - delete a group
* newgrp - log in to a new group
* passwd - change user password
* gpasswd - administer /etc/group and /etc/gshadow
* usermod - modify a user account
* chfn - change real user name and information
* chsh - change login shell
* groupmod - modify a group definition on the system
* lastlog - reports the most recent login of all users or of a given user
* last, lastb - show a listing of last logged in users
* users - print the user names of users currently logged in to the current host
* groups - print the groups a user is in
* id - print real and effective user and group IDs
