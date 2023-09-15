# 🌐 Deploying an Website on Apache2 Server in Amazon Ec2🚀

This detailed guide will walk you through deploying an HTML website using Apache2 on a Linux-based system, with Ubuntu as the example. Each command is explained along with appropriate emojis to make it more enjoyable! 😊

## 🌐 Website Deployment Requirements Checklist 🚀

### **1. AWS Instance Requirements**

- **Instance Type:** t2.micro
  - ⚙️ Use a t2.micro instance for cost-effective hosting.

- **Operating System:** Ubuntu 20.04 or above
  - 🐧 Ubuntu OS for web hosting

### **2. Security Group Rules**

- **SSH Access (Port 22):**
  - Allow Inbound Rules from *your IP address only* (MyIP).
  - ✅ Ensure secure SSH access.

- **HTTP Access (Port 80):**
  - Allow Inbound Rules from *Anywhere* (0.0.0.0/0).
  - 🌍 Enable public access to your website.

By following these requirements and naming conventions, you can set up a secure and well-organized environment for deploying your website on AWS. Enjoy your web hosting journey! 🌟🌐🔒

### 1. Update Package List 🔄
```bash
sudo apt update
```
- **Description:** This command updates the package list on your system, ensuring you have access to the latest software packages.

### 2. Create a Deployment Directory 📂
```bash
mkdir website_Deployment
cd website_Deployment/
```
- **Description:** This command creates a directory called "website_Deployment" and navigates into it. You can choose any directory name you prefer.

### 3. Install Apache2 Web Server ⚙️
```bash
sudo apt install apache2 -y
```
- **Description:** This command installs the Apache2 web server, widely used for serving web content.

### 4. Start Apache2 Service ▶️
```bash
sudo systemctl start apache2
```
- **Description:** This command starts the Apache2 service so it can begin serving web content.

### 5. Enable Apache2 to Start on Boot 🚗
```bash
sudo systemctl enable apache2
```
- **Description:** This command configures Apache2 to start automatically when the system boots up.

### 6. Check Apache2 Service Status 📊
```bash
sudo systemctl status apache2
```
- **Description:** This command checks the status of the Apache2 service, ensuring it is running without errors.

### 7. Check Your Server's Public IP Address 🌐
```bash
curl http://checkip.amazonaws.com
```
- **Description:** This command retrieves your server's public IP address from the "checkip.amazonaws.com" service. Useful for accessing your website from the internet. 
    > Copy the IP Address in Browser and you are able to see default Apache2 index page

### 8. Prepare HTML Content 📝
```bash
ls /var/www/html/
echo "Learning DevOps" > index.html
cat index.html
```
- **Description:** These commands create a simple HTML file named "index.html" with the content "Learning DevOps" and display its contents.

### 9. Remove Default Apache2 Index Page 🗑️
```bash
sudo rm -r /var/www/html/index.html
```
- **Description:** This command removes the default Apache2 index page to prepare for the deployment of your HTML website.

### 10. Copy Your HTML Content to Apache2's Document Root 📂
```bash
sudo cp index.html /var/www/html/
```
- **Description:** This command copies your "index.html" file to the Apache2 document root directory, where your website content will be served from.

### 11. Verify Your Website ✅
```bash
cat /var/www/html/index.html 
```
- **Description:** This command displays the content of the "index.html" file to verify that it has been successfully copied.

### 12. Restart Apache2 to Apply Changes 🔄
```bash
sudo systemctl restart apache2
```
- **Description:** This command restarts the Apache2 service to apply the changes made to the website content.

### 13. Install wget and unzip 🌐
```bash
sudo apt install wget unzip -y
```
- **Description:** This command installs the "wget" and "unzip" utilities, which will be used to download and extract website templates.

### 14. Download a Website Template 📥
```bash
wget https://www.tooplate.com/zip-templates/2126_antique_cafe.zip
```
- **Description:** This command downloads a website template in ZIP format from the specified URL. Replace the URL with your preferred template.

### 15. List Files in the Current Directory 📂
```bash
ls
```
- **Description:** This command lists the files in the current directory to verify that the ZIP file has been downloaded.

### 16. Extract the Website Template 📦
```bash
unzip 2126_antique_cafe.zip
```
- **Description:** This command extracts the downloaded ZIP file, containing the website template files.

### 17. Replace Template Content 🔄
Replace `yourname` in the below command with your desired name.
```bash
sed -i 's/Antique/yourname/g' 2126_antique_cafe/index.html
```
- **Description:** This command uses the `sed` command to replace the word "Antique" with "yourname" in the template's HTML file. Replace "yourname" with your desired website name.

### 18. Remove Default Apache2 Index Page (Again) 🗑️
```bash
sudo rm -r /var/www/html/index.html
```
- **Description:** This command removes the previous "index.html" file to prepare for the template deployment.

### 19. Copy Template Files to Apache2 Document Root 📂
```bash
sudo cp -r 2126_antique_cafe/* /var/www/html/
```
- **Description:** This command copies all files and directories from the extracted template folder to the Apache2 document root directory, deploying your website.

### 20. Restart Apache2 to Apply Changes (Again) 🔄
```bash
sudo systemctl restart apache2
```
- **Description:** This command restarts the Apache2 service to apply the changes made during the template deployment.

### 21. Verify Your Website Again ✅
```bash
curl http://checkip.amazonaws.com
```
- **Description:** This command retrieves your server's public IP address, allowing you to access your newly deployed website.

Congratulations! You've successfully deployed an HTML website on Apache2. Access your website using your server's public IP address and share it with the world! 🎉🌍
