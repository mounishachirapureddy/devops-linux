# Understand Linux Directory Structure
> Ref: https://linuxhandbook.com/linux-directory-structure/

> Ref: https://www.youtube.com/watch?v=42iQKuQodW4&ab_channel=Fireship

> Ref: https://www.youtube.com/watch?v=HbgzrKJvDRw&ab_channel=DorianDotSlash
---
## Navigating the Linux File System Hierarchy 📁🐧

The Linux File System Hierarchy is a structured organization of directories and files that forms the backbone of the Linux operating system. It is designed to provide a clear and organized way to manage system resources and user data. In this detailed description, we will explore the key directories within the Linux File System Hierarchy, their purposes, and the common commands and use cases associated with them.

---
**/** - The Root Directory 🌳
   - **Description**: The root directory is the top-level directory in a Unix/Linux file system, serving as the starting point for all paths.
   - **Use Case**: The foundation and root of all directories and files in Linux.
   - **Example**: /
---
**/bin** - Essential System Binaries 📦
   - **Description**: /bin contains essential command binaries required for system boot and basic recovery, providing core system functionality.
   - **Use Case**: Crucial for basic system functionality, hosting commands like `ls` and `cat`.
   - **Example**: /bin/ls, /bin/cat
---
**/dev** - Device Files 🖥️
   - **Description**: /dev houses device files that represent both physical and virtual devices, enabling hardware communication.
   - **Use Case**: Facilitates device communication and management; e.g., `/dev/null` for discarding data.
   - **Example**: /dev/sda (represents a hard disk), /dev/null (null device)
---
**/etc** - System Configuration Files ⚙️
   - **Description**: /etc stores system-wide configuration files for applications and services, controlling system behavior.
   - **Use Case**: Centralized storage for configuration settings, e.g., `/etc/ssh/sshd_config`.
   - **Example**: /etc/ssh/sshd_config, /etc/network/interfaces
---
**/usr** - User Binaries and Program Data 👤📊
   - **Description**: /usr contains user-specific binaries, libraries, and program data, shared across users.
   - **Use Case**: Hosts software and data accessible to all users, e.g., `/usr/bin/gcc`.
   - **Example**: /usr/bin/gcc, /usr/share/applications/firefox.desktop
---
**/home** - User Home Directories 🏠
   - **Description**: /home stores individual users' personal data and configuration files, ensuring privacy and customization.
   - **Use Case**: Secured location for user-specific files, e.g., `/home/johndoe`.
   - **Example**: /home/johndoe
---
**/lib** - Shared Libraries 📚
   - **Description**: /lib contains shared libraries used by various programs, optimizing code sharing.
   - **Use Case**: Efficiency in code sharing among programs, e.g., `/lib/libc.so.6`.
   - **Example**: /lib/libc.so.6, /lib64/ld-linux-x86-64.so.2
---
**/sbin** - System Binaries for Administration ⚙️📦
   - **Description**: Similar to /bin, /sbin contains binaries for system administration tasks, essential for maintenance and recovery.
   - **Use Case**: Crucial for system administration; e.g., `/sbin/ifconfig` and `/sbin/reboot`.
   - **Example**: /sbin/ifconfig, /sbin/reboot
---
**/tmp** - Temporary Files and Directories 🗑️
   - **Description**: /tmp stores temporary files created by the system and applications, ideal for short-term data.
   - **Use Case**: Used for temporary storage and sharing, e.g., `/tmp/session-1234`.
   - **Example**: /tmp/session-1234
---
**/var** - Variable Data Files and Logs 📁🔄
   - **Description**: /var holds variable data like log files, mail spools, and databases, reflecting dynamic system changes.
   - **Use Case**: Stores changing data and system event logs, e.g., `/var/log/syslog`.
   - **Example**: /var/log/syslog, /var/spool/mail/user
---
**/boot** - Boot Files 🖥️👢
   - **Description**: /boot contains boot loader configuration and kernel files, crucial for system startup.
   - **Use Case**: Essential for system booting, e.g., `/boot/grub/grub.cfg`.
   - **Example**: /boot/grub/grub.cfg
---
**/proc** - Process and Kernel Files 🔄🧠
   - **Description**: /proc contains virtual files representing system and process information, providing real-time data.
   - **Use Case**: Offers insight into running processes and kernel parameters, e.g., `/proc/cpuinfo`.
   - **Example**: /proc/cpuinfo, /proc/meminfo
---
**/opt** - Optional Software 🛠️
   - **Description**: /opt is used for installing optional software packages separately from the core system.
   - **Use Case**: Organizes optional software without affecting the core system, e.g., `/opt/google/chrome`.
   - **Example**: /opt/google/chrome
---
**/root** - The Home Directory of the Root 🏠👑
   - **Description**: /root serves as the home directory for the system administrator (root), containing their personal configuration and data.
   - **Use Case**: Root user's private space, e.g., `/root`.
   - **Example**: /root
---
**/media** - Mount Point for Removable Media 📀🔌
   - **Description**: /media acts as a temporary mount point for removable devices like USB drives, facilitating access.
   - **Use Case**: Allows easy mounting and access to removable media, e.g., `/media/usb_drive`.
   - **Example**: /media/usb_drive
---
**/mnt** - General Mount Directory 🌄
   - **Description**: /mnt serves as a generic mount point for manually mounting filesystems, providing flexibility.
   - **Use Case**: Manual mounting of additional storage or network shares, e.g., `/mnt/data`.
   - **Example**: /mnt/data
---
**/srv** - Service Data 🚀
   - **Description**: /srv contains data related to services provided by the system, enabling efficient service management.
   - **Use Case**: Stores data served by various system services, e.g., `/srv/www` for web server content.
   - **Example**: /srv/www
