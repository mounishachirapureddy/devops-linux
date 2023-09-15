# Software Package Management in Linux 🐧📦

In the world of Linux, efficient package management is crucial for installing, updating, and maintaining software on your system. Different Linux distributions employ various package managers to facilitate this process. Below, we provide an overview of two widely used package managers and their respective commands: rpm (Red Hat Package Manager) for Red Hat-based distributions, and dpkg (Debian Package) for Debian-based distributions, like Ubuntu.

#### `rpm` (Red Hat Package Manager)
- **Description**: `rpm` is the default package manager for Red Hat-based Linux distributions like Fedora, CentOS, and RHEL. It is used for installing, querying, and managing individual software packages.
- **Example Install**: `sudo rpm -i package.rpm`
- **Example Remove**: `sudo rpm -e package_name`
- **Example Query**: `rpm -q package_name`
- **Example List Installed Packages**: `rpm -qa`
- **Install `tree` using `rpm`**: `sudo rpm -i tree.rpm`

#### `dpkg` (Debian Package)
- **Description**: `dpkg` is the default package manager for Debian-based Linux distributions like Ubuntu and Debian. It is used for installing, querying, and managing individual software packages.
- **Example Install**: `sudo dpkg -i package.deb`
- **Example Remove**: `sudo dpkg -r package_name`
- **Example Purge (Remove and Purge Configuration Files)**: `sudo dpkg -P package_name`
- **Example Query**: `dpkg -l | grep package_name`
- **Install `tree` using `dpkg`**: `sudo dpkg -i tree.deb`

#### `apt` vs. `dpkg`
- **Description**: `apt` is a higher-level package management tool that sits on top of `dpkg`. It resolves dependencies and can download and install packages from repositories.
- **Example Install with `apt`**: `sudo apt-get install package_name`
- **Example Remove with `apt`**: `sudo apt-get remove package_name`

#### `yum` vs. `rpm`
- **Description**: `yum` is a higher-level package management tool that sits on top of `rpm`. It resolves dependencies and can download and install packages from repositories.
- **Example Install with `yum`**: `sudo yum install package_name`
- **Example Remove with `yum`**: `sudo yum remove package_name`

## Installing Different Tools/Languages on Linux 🐧

Learn about default package managers for different Linux distributions and how to install various tools, web servers, programming languages, databases, and search for packages. 📦🚀

## Default Package Managers 📦

#### Ubuntu/Debian
- **Package Manager**: `apt` 
- **Repository Configuration**: `/etc/apt/sources.list`, `/etc/apt/sources.list.d/`
- **Update Packages**: `apt update`, `apt upgrade`
- **Install Packages**: `apt install package_name`
- **Remove Packages**: `apt remove package_name`
- **Search for Packages**: `apt-cache search package_name`
- **Purge Packages (Remove and Purge Configuration Files)**: `apt remove --purge package_name`
- **Enable Service at Boot**: `sudo systemctl enable service_name`
- **Disable Service at Boot**: `sudo systemctl disable service_name`
- **Check if Service is Enabled at Boot**: `sudo systemctl is-enabled service_name`
- **Check if Service is Disabled at Boot**: `sudo systemctl is-disabled service_name`

#### Fedora/CentOS/RHEL
- **Package Manager**: `yum`
- **Alternative Package Manager (RHEL 8+)**: `dnf`
- **Repository Configuration**: `/etc/yum.repos.d/`
- **Update Packages**: `yum update`
- **Install Packages**: `yum install package_name` or `dnf install package_name`
- **Remove Packages**: `yum remove package_name` or `dnf remove package_name`
- **Search for Packages**: `yum search package_name` or `dnf search package_name`
- **Purge Packages (Remove and Purge Configuration Files)**: `yum remove --purge package_name` or `dnf remove --purge package_name`
- **Enable Service at Boot**: `sudo systemctl enable service_name`
- **Disable Service at Boot**: `sudo systemctl disable service_name`
- **Check if Service is Enabled at Boot**: `sudo systemctl is-enabled service_name`
- **Check if Service is Disabled at Boot**: `sudo systemctl is-disabled service_name`

#### Alpine
- **Package Manager**: `apk`
- **Repository Configuration**: `/etc/apk/repositories`
- **Install Packages**: `apk add package_name`
- **Remove Packages**: `apk del package_name`
- **Search for Packages**: `apk search package_name`
- **Purge Packages (Remove and Purge Configuration Files)**: `apk del --purge package_name`
- **Enable Service at Boot**: `sudo rc-update add service_name`
- **Disable Service at Boot**: `sudo rc-update del service_name`
- **Check if Service is Enabled at Boot**: Not applicable
- **Check if Service is Disabled at Boot**: Not applicable

### Install Web Servers 🌐

#### 1. Install Nginx Web Server
- **Installation**:
  ```bash
  sudo yum install nginx  # For Fedora/CentOS/RHEL
  sudo apt install nginx  # For Ubuntu/Debian
  sudo apk add nginx  # For Alpine
  ```
- **Check Server Status**:
  - Visit `localhost:80` in a web browser.
- **Check PID and Status**:
  ```bash
  ps aux | grep nginx
  ```
- **Stop, Start, Restart Nginx**:
  ```bash
  sudo systemctl stop nginx
  sudo systemctl start nginx
  sudo systemctl restart nginx
  ```
- **Serve a Custom HTML Page**:
  - Place your HTML file in `/usr/share/nginx/html/`.
- **Create a Virtual Host (mywebsite.com)**:
  - Configure Nginx server block.
- **Map the Website to localhost**:
  - Edit `/etc/hosts` and add an entry like `127.0.0.1 mywebsite.com`.
- **Uninstall Nginx Completely**:
  ```bash
  sudo yum remove --purge nginx  # For Fedora/CentOS/RHEL
  sudo apt remove --purge nginx  # For Ubuntu/Debian
  sudo apk del --purge nginx  # For Alpine
  ```

#### 2. Install Apache Web Server
- **Installation**:
  ```bash
  sudo yum install httpd  # For Fedora/CentOS/RHEL
  sudo apt install apache2  # For Ubuntu/Debian
  sudo apk add apache2  # For Alpine
  ```
- **Check Server Status**:
  - Visit `localhost:80` in a web browser.
- **Check PID and Status**:
  ```bash
  ps aux | grep apache
  ```
- **Stop, Start, Restart Apache**:
  ```bash
  sudo systemctl stop httpd
  sudo systemctl start httpd
  sudo systemctl restart httpd
  ```
- **Uninstall Apache Completely**:
  ```bash
  sudo yum remove --purge httpd  # For Fedora/CentOS/RHEL
  sudo apt remove --purge apache2  # For Ubuntu/Debian
  sudo apk del --purge apache2  # For Alpine
  ```

### Install Different Languages 🚀

#### 1. Install Java
- **Installation (Java 17)**:
  ```bash
  sudo yum install java-17-openjdk  # For Fedora/CentOS/RHEL
  sudo apt install openjdk-17-jdk  # For Ubuntu/Debian
  sudo apk add openjdk17  # For Alpine
  ```
- **Run a Simple Java Program**:
  ```java
  public class HelloWorld {
      public static void main(String[] args) {
          System.out.println("Hello, World!");
      }
  }
  ```
- **Uninstall Java Completely**:
  ```bash
  sudo yum remove --purge java-17-openjdk  # For Fedora/CentOS/RHEL
  sudo apt remove --purge openjdk-17-jdk  # For Ubuntu/Debian
  sudo apk del --purge openjdk17  # For Alpine
  ```

#### 2. Install Ruby
- **Installation (Ruby 3.0)**:
  ```bash
  sudo yum install ruby  # For Fedora/CentOS/RHEL
  sudo apt install ruby  # For Ubuntu/Debian
  sudo apk add ruby  # For Alpine
  ```
- **Run a Simple Ruby Program**:
  ```ruby
  puts "Hello, Ruby!"
  ```
- **Uninstall Ruby Completely**:
  ```bash
  sudo yum remove --purge ruby  # For Fedora/CentOS/RHEL
  sudo apt remove --purge ruby  # For Ubuntu/Debian
  sudo apk del --purge ruby  # For Alpine
  ```

#### 3. Install Python 3
- **Installation (Using pyenv)**:
  ```bash
  sudo yum install pyenv  # For Fedora/CentOS/RHEL
  sudo apt install pyenv  # For Ubuntu/Debian
  sudo apk add pyenv  # For Alpine
  ```
- **Run a Simple Python Program**:
  ```python
  print("Hello, Python!")
  ```
- **No Need to Uninstall Python (Can cause issues on Ubuntu)**.

### Install Databases

 📊

#### 1. Install MySQL
- **Installation (MySQL 8.x)**:
  ```bash
  sudo yum install mysql-server  # For Fedora/CentOS/RHEL
  sudo apt install mysql-server  # For Ubuntu/Debian
  sudo apk add mysql-server  # For Alpine
  ```
- **Login to MySQL**:
  ```bash
  mysql -u root -p
  ```
- **List Existing Databases and Exit MySQL**:
  ```sql
  SHOW DATABASES;
  EXIT;
  ```
- **Uninstall MySQL Completely**:
  ```bash
  sudo yum remove --purge mysql-server  # For Fedora/CentOS/RHEL
  sudo apt remove --purge mysql-server  # For Ubuntu/Debian
  sudo apk del --purge mysql-server  # For Alpine
  ```

#### 2. Install PostgreSQL
- **Installation (PostgreSQL 8.x)**:
  ```bash
  sudo yum install postgresql-server  # For Fedora/CentOS/RHEL
  sudo apt install postgresql-server  # For Ubuntu/Debian
  sudo apk add postgresql-server  # For Alpine
  ```
- **Login to PostgreSQL**:
  ```bash
  sudo -u postgres psql
  ```
- **List Existing Databases and Exit PostgreSQL**:
  ```sql
  \l
  \q
  ```
- **Uninstall PostgreSQL Completely**:
  ```bash
  sudo yum remove --purge postgresql-server  # For Fedora/CentOS/RHEL
  sudo apt remove --purge postgresql-server  # For Ubuntu/Debian
  sudo apk del --purge postgresql-server  # For Alpine
  ```

### Install Python Packages with `pip` 🐍

#### 1. Install `pip`
- **Installation**:
  ```bash
  sudo yum install python3-pip  # For Fedora/CentOS/RHEL
  sudo apt install python3-pip  # For Ubuntu/Debian
  sudo apk add py3-pip  # For Alpine
  ```

#### 2. Install Python Packages
- **Installation**:
  ```bash
  sudo pip3 install package_name
  ```
- **Uninstall Python Packages**:
  ```bash
  sudo pip3 uninstall package_name
  ```

Now, you have comprehensive instructions on installing, managing, searching for packages, purging packages, enabling/disabling services, various tools, web servers, programming languages, databases, and Python packages on Linux systems. Enjoy exploring and working with these technologies! 🌐💻📊🐍
