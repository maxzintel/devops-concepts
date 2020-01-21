# Linux File Systems:
# File Systems in Linux
A list of the important file systems in Linux OS and what they are for.

* `/bin` = binaries
  * Apps and programs you can run. Basic tools for making/removing/moving files and directories.
* `/boot` = system startup
  * Don't touch it.
* `/dev` = device files
  * Device files are created on boot or on the fly. Ex: plugging in a webcam.
* `/etc` = formerly et cetera
  * Now 'everything to config'. Config files, usernames, passwords, hard disk partitions.
* `/home` = users personal directories
* `/lib` = libraries
  * Code for apps to use.
* `/media` = external storage
* `/mnt` = old storage mount
* `/opt` = software we compile/build
  * /opt/bin <=> /usr/local/bin
  * /opt/lib <=> /usr/local/lib
* `/proc` = like /dev
  * But for info about CPU and kernel.
* `/root` = /home of admin
  * Don't touch it.
* `/run` = system processes
  * Used for storage of temporary data.
  * Don't touch it.
* `/sbin` = bin for super user
* `/usr` = apps, libs, dirs, wallpapers, icons, etc...
* `/srv` = server data
* `/sys` = like /dev and /proc but for devs connected to your machine.
  * Don't touch it.
* `/tmp` = temp for running applications
  * No need for sudo. Can touch this!
* `/var` = variable
  * For logs (/var/log). Captures kernel failures, break-in attempts, task spools (like for printing).
