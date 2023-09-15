# Linux Basic Commands Cheatsheet 🐧
> Ref: [DigitalOcean Linux Commands](https://www.digitalocean.com/community/tutorials/linux-commands#the-pwd-command-in-linux)

> Ref: [GeeksforGeeks Basic Linux Commands](https://www.geeksforgeeks.org/basic-linux-commands/)
---
## Basic File Commands 📁

### File Navigation
- **ls** - List directories and files 📂
  > Example: 
    ```bash
    ls
    ```
  > Use Case: To list the contents of the current directory.
- **ls -a** - List all files and directories, including hidden ones 🕵️
  > Example:
    ```bash
    ls -a
    ```
  > Use Case: To list all files and directories, including hidden ones.
- **ls -l** - List files and directories in long format 📃
  > Example:
    ```bash
    ls -l
    ```
  > Use Case: To list files and directories in long format.
- **pwd** - Print Working Directory 🗂️
  > Example:
    ```bash
    pwd
    ```
  > Use Case: To display the current working directory.
- **cd** - Change Directory 🚶‍♂️
  > Example:
    ```bash
    cd /path/to/directory
    ```
  > Use Case: To navigate to a different directory.
---
### File Management
- **mkdir** - Create a new directory 📂
  > Example:
    ```bash
    mkdir new_directory
    ```
  > Use Case: To create a new directory.
- **mv** - Move or rename files and directories 🔄
  > Example:
    ```bash
    mv file1 file2
    ```
  > Use Case: To move or rename files and directories.
- **cp** - Copy files and directories 📄
  > Example:
    ```bash
    cp file1 file2
    ```
  > Use Case: To create copies of files and directories.
- **rm** - Remove files and directories 🗑️
  > Example:
    ```bash
    rm file.txt
    ```
  > Use Case: To delete files or directories.
- **touch** - Create blank/empty files 📝
  > Example:
    ```bash
    touch new_file.txt
    ```
  > Use Case: To create empty files.
- **ln** - Create symbolic links (shortcuts) to other files 🔗
  > Example:
    ```bash
    ln -s source_file link_name
    ```
  > Use Case: To create symbolic links to files or directories.
---
## Filters and Redirections 🌪️

### Text Filtering
- **grep** - Search for a string or pattern within text files 🔍
  > Example:
    ```bash
    grep "search_term" file.txt
    ```
  > Use Case: To search for a specific string or pattern in a text file.
- **grep -i** - Perform a case-insensitive search 🔄
  > Example:
    ```bash
    grep -i "pattern" file.txt
    ```
  > Use Case: To perform a case-insensitive search.
- **awk** - Text processing tool for data extraction and reporting 📊
  > Example:
    ```bash
    awk '/pattern/ {print $1}' file.txt
    ```
  > Use Case: To extract and manipulate data from text files.
- **pipe (|)** - Redirect the output of one command as input to another 🚀
  > Example:
    ```bash
    command1 | command2
    ```
  > Use Case: To send the output of `command1` as input to `command2`.
---
### Text Manipulation
- **sed** - Stream editor for text manipulation 📝
  > Example:
    ```bash
    sed 's/old_text/new_text/g' file.txt
    ```
  > Use Case: To perform text substitution and manipulation.
- **sed -i** - Edit files in-place with sed 📝
  > Example:
    ```bash
    sed -i 's/old_text/new_text/g' file.txt
    ```
  > Use Case: To edit files in-place with sed.
---
### Redirection
- **>** - Redirect output to a file 📄
  > Example:
    ```bash
    command > output.txt
    ```
  > Use Case: To redirect the standard output to a file.
- **>>** - Append output to a file 📄
  > Example:
    ```bash
    command >> output.txt
    ```
  > Use Case: To append the standard output to a file.
- **2>** - Redirect error output to a file 📄
  > Example:
    ```bash
    command 2> error.txt
    ```
  > Use Case: To redirect error output to a file.
- **&>>** - Redirect both standard and error output to a file 📄
  > Example:
    ```bash
    command &>> output.txt
    ```
  > Use Case: To redirect both standard and error output to a file.
---
## File Content Display and Manipulation 📄

### Displaying File Content
- **cat** - Display file contents on the terminal 📃
  > Example:
    ```bash
    cat file.txt
    ```
  > Use Case: To display the contents of a file.
- **less** - Display paged outputs in the terminal 📜
  > Example:
    ```bash
    less large_file.txt
    ```
  > Use Case: To view large files page by page.
- **more** - Display file contents one screen at a time 📃
  > Example:
    ```bash
    more file.txt
    ```
  > Use Case: To view file contents page by page.
- **head** - Display the first few lines of a file 📜
  > Example:
    ```bash
    head -n 10 file.txt
    ```
  > Use Case: To display the first few lines of a file.
- **tail** - Display the last few lines of a file 📚
  > Example:
    ```bash
    tail -n 10 file.txt
    ```
  > Use Case: To display the last few lines of a file.
---
### File Comparison
- **diff** - Find the difference between two files 📊
  > Example:
    ```bash
    diff file1.txt file2.txt
    ```
  > Use Case: To compare two files and find differences.
- **cmp** - Check if two files are identical ☑️
  > Example:
    ```bash
    cmp file1.txt file2.txt
    ```
  > Use Case: To check if two files are identical.
- **comm** - Compare two sorted files line by line 📝
  > Example:
    ```bash
    comm file1.txt file2.txt
    ```
  > Use Case: To compare two sorted files line by line.
---
### File Sorting
- **sort** - Sort the content of a file while outputting 📝
  > Example:
    ```bash
    sort file.txt
    ```
  > Use Case: To sort the contents of a file.
---
### File Compression and Archiving 🗃️
- **tar** - Extract and compress files 📦
  > Example:
    ```bash
    tar -zxvf archive.tar.gz
    ```
  > Use Case: To extract or compress files and directories.
- **zip** - Zip files 🗃️
  > Example:
    ```bash
    zip archive.zip file1 file2
    ```
  > Use Case: To create a compressed archive.
- **unzip** - Unzip files 📦
  > Example:
    ```bash
    unzip archive.zip
    ```
  > Use Case: To extract files from a ZIP archive.
---
## User Commands 👤

### User Management
- **useradd** - Add a new user 👤
  > Example:
    ```bash
    useradd newuser
    ```
  > Use Case: To create a new Linux user.
- **usermod** - Modify user account properties 🛠️
  > Example:
    ```bash
    usermod -aG groupname username
    ```
  > Use Case: To modify user account properties, like adding a user to a group.
- **passwd** - Set or change user password 🔐
  > Example:
    ```bash
    passwd username
    ```
  > Use Case: To set or change user passwords.
- **sudo** - Run a command with superuser privileges 🔑
  > Example:
    ```bash
    sudo command
    ```
  > Use Case: To execute a command with elevated privileges.
---
### User Deletion
- **userdel** - Delete a user account 👋
  > Example:
    ```bash
    userdel username
    ```
  > Use Case: To delete an existing user account.
---
### Permissions
- **chmod** - Change file permissions 🔒
  > Example:
    ```bash
    chmod 755 file.txt
    ```
  > Use Case: To change file permissions.
- **chown** - Change file ownership 🤲
  > Example:
    ```bash
    chown user:group file.txt
    ```
  > Use Case: To change file ownership.
---
## Miscellaneous Commands 🌐

### Network
- **ifconfig** - Display network interfaces and IP addresses 🌐
  > Example:
    ```bash
    ifconfig
    ```
  > Use Case: To view network configuration.
- **traceroute** - Trace network hops to a destination 🌐
  > Example:
    ```bash
    traceroute example.com
    ```
  > Use Case: To trace the route packets take to reach a destination.
- **wget** - Directly download files from the internet 🌐
  > Example:
    ```bash
    wget http://example.com/file.txt
    ```
  > Use Case: To download files from the internet.
- **ssh** - Connect to a remote server securely 🔐
  > Example:
    ```bash
    ssh user@hostname
    ```
  > Use Case: To establish a secure shell connection to a remote server.
---
### Process Management
- **ps** - Display active processes 🔄
  > Example:
    ```bash
    ps aux
    ```
  > Use Case: To view a list of running processes.
- **kill** - Terminate processes by process ID ☠️
  > Example:
    ```bash
    kill process_id
    ```
  > Use Case: To terminate processes by their ID.
- **killall** - Terminate processes by name ☠️
  > Example:
    ```bash
    killall process_name
    ```
  > Use Case: To terminate processes by their name.
- **top** - Monitor active processes and system usage 📊
  > Example:
    ```bash
    top
    ```
  > Use Case: To monitor active processes and system usage.
---
### System Information
- **uname** - Get basic information about the OS ℹ️
  > Example:
    ```bash
    uname -a
    ```
  > Use Case: To get information about the operating system.
- **whoami** - Display the active username 👤
  > Example:
    ```bash
    whoami
    ```
  > Use Case: To display the username of the currently logged-in user.
---
### Firewall
- **ufw** - Manage the Uncomplicated Firewall 🔥
  > Example:
    ```bash
    ufw enable
    ```
  > Use Case: To manage the Uncomplicated Firewall.
- **iptables** - Configure advanced firewall rules 🔒
  > Example:
    ```bash
    iptables -A INPUT -p tcp --dport 80 -j ACCEPT
    ```
  > Use Case: To configure advanced firewall rules.
---
### Package Management 📦
- **apt, pacman, yum, rpm** - Package managers depending on the distro 📦
  > Example:
    ```bash
    apt install package_name
    ```
  > Use Case: To manage software packages.
---
### Customization and Utilities
- **alias** - Create custom shortcuts for regularly used commands ✨
  > Example:
    ```bash
    alias ll='ls -l'
    ```
  > Use Case: To create custom command shortcuts.
- **cal** - View a command-line calendar 📅
  > Example:
    ```bash
    cal
    ```
  > Use Case: To view a calendar in the terminal.
- **dd** - Create bootable USB drives from disk images 📦
  > Example:
    ```bash
    dd if=image.iso of=/dev/sdX bs=4M status=progress
    ```
  > Use Case: To create bootable USB drives from disk images.
- **whereis** - Locate the binary, source, and manual pages for a command 🔍
  > Example:
    ```bash
    whereis ls
    ```
  > Use Case: To find the binary, source, and manual pages for a command.
- **whatis** - Find a brief description of a command ℹ️
  > Example:
    ```bash
    whatis ls
    ```
  > Use Case: To find a brief description of a command.
---
## System Administration and Advanced Commands 🛠️

### File Search and Management
- **find** - Search for files and directories within a specified location 🔍
  > Example:
    ```bash
    find /path/to/search -name "filename"
    ```
  > Use Case: To search for files and directories by name or other criteria.
- **du** - Display disk usage of files and directories 📊
  > Example:
    ```bash
    du -sh /path/to/directory
    ```
  > Use Case: To check the disk space used by files and directories.
---
### System Maintenance
- **history** - View a list of previously executed commands 🕒
  > Example:
    ```bash
    history
    ```
  > Use Case: To view the command history for the current user.
- **at** - Schedule tasks to run at a specific time ⏰
  > Example:
    ```bash
    at 2:00 PM tomorrow
    ```
  > Use Case: To schedule tasks to run at a specified time.
- **cron** - Schedule recurring tasks 🔄
  > Example:
    ```bash
    crontab -e
    ```
  > Use Case: To schedule automated tasks.
- **shutdown** - Power off or restart the system 🚀
  > Example:
    ```bash
    shutdown -h now
    ```
  > Use Case: To power off the system immediately.
- **reboot** - Restart the system 🔄
  > Example:
    ```bash
    reboot
    ```
  > Use Case: To restart the system.

Now you have an extensive Linux commands cheatsheet covering a wide range of commands for various tasks. 🚀🐧

---
## Understand users 🧑‍💻
- Creating a new Linux user 👤
- Removing an existing user 👋
- Giving permissions for a file/directory to a user 🔒
- Making a user as sudo user 👑

## Understand permissions 🔐
- Checking existing file permissions 🔍
- Changing permissions to a file/directory 🔒
- Making a script executable 🚀
