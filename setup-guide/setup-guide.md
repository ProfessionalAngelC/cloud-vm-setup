# AWS Windows VM Setup Guide

## 1. EC2 Instance Creation
1. Log in to AWS Management Console
2. Navigate to EC2 → Launch Instance
3. Choose **AMI**: Windows Server 2022
4. Choose **Instance Type**: t2.micro (free tier)
5. Configure Network & Security:
   - Security group rules: **RDP (3389)**
   - Optional: **HTTP (80)** for web server testing
6. Add storage: 30GB default (free tier), optional extra 10GB
7. Add tags: Key = `Name`, Value = `Portfolio-Windows-VM`
8. Launch instance → Create new key pair (download `.pem`)

---

## 2. Connect to VM
1. Open **Remote Desktop Connection** on your Windows laptop
2. Enter **Public IP** of your EC2 instance
3. Username: `Administrator`
4. Password: Retrieve from AWS console (“Get Password” using your key pair)

---

## 3. IIS Web Server Setup
1. Open **Server Manager**
2. Click **Add Roles and Features**
3. Select **Web Server (IIS)** → Install
4. After installation, open **Internet Explorer** inside VM:
   - Go to `http://localhost`  
   - You should see the IIS “Welcome” page

---

## 4. Optional Storage Volume (EBS)
1. In AWS Console → EC2 → Volumes → Create Volume → Attach to instance
2. Inside VM: Open **Disk Management**
3. Initialize the disk and assign a drive letter (e.g., `E:`)
4. Confirm the volume is accessible in **This PC**

---

## 5. Testing
- RDP connection works
- Web server accessible at `http://<Public-IP>`
- Storage volume visible inside VM
