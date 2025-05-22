# 🖥️ Windows Server 2025 Domain Controller Lab (VirtualBox)

This project demonstrates the installation and configuration of a Windows Server 2025 virtual machine on VirtualBox, with the setup of a Domain Controller using Active Directory Domain Services (AD DS). It’s part of a home lab aimed at strengthening IT support and system administration skills.

---

## 🎯 Objectives

- Install Windows Server 2025 on a VirtualBox virtual machine.
- Configure basic network settings to support domain services.
- Promote the server to a Domain Controller using Active Directory Domain Services.
- Create and manage domain users and organizational units.
- Join a Windows 10 client VM to the domain (optional extension).

---

## 🧰 Tools Used

- **Oracle VirtualBox** – Virtualization platform
- **Windows Server 2025 ISO** – Operating system
- **Active Directory Domain Services (AD DS)** – Role on Windows Server

---

## 🪜 Steps Taken

### 1. **Prepare the Environment**
- Download and install VirtualBox.
- Download Windows Server 2025 Evaluation ISO from Microsoft.

### 2. **Create a New Virtual Machine**
- Name: `WinServer2025-DC`
- Type: `Microsoft Windows`
- Version: `Windows 2025 (64-bit)`
- RAM: `4GB` minimum
- Hard disk: `50GB` dynamically allocated

### 3. **Install Windows Server 2025**
- Boot from the ISO.
- Choose Standard Installation (Desktop Experience).
![01-Install Windows Server](https://github.com/user-attachments/assets/ee1ea034-90fc-4aaa-8ded-c46e58c91c9a)


- Set local admin password.

![02 - Admin Password](https://github.com/user-attachments/assets/67af1e30-4983-4309-9b34-4ef8a4349b4d)


  ![03-Enter Password](https://github.com/user-attachments/assets/0759c449-143c-49a1-b9ea-a33f2fce5245)


### 4. **Initial Configuration**
- Set static IP address (for AD DS).
<img width="822" alt="14-Change settings" src="https://github.com/user-attachments/assets/28f7ee87-3b99-4598-b344-92ccb5cf4292" />


<img width="626" alt="16-properties" src="https://github.com/user-attachments/assets/9dcd4283-3718-4beb-9566-9a62a12c62bc" />


<img width="257" alt="17-IPv4" src="https://github.com/user-attachments/assets/74399b76-ea45-49b5-87d7-1b8987cd24bf" />


- Rename the computer (`DC01`).

<img width="329" alt="15-DC01" src="https://github.com/user-attachments/assets/7de7719e-bbc8-457e-9b87-8c21df97f675" />

- Update Windows and install VirtualBox Guest Additions.

![04-Guest Additions](https://github.com/user-attachments/assets/7011a964-4438-413d-acfe-e738b57534af)


![05-Guest Additions](https://github.com/user-attachments/assets/0294fe38-5145-4690-8ade-f721d101869f)

### 5. **Install Active Directory Domain Services**
- Open Server Manager → Add Roles and Features.
<img width="824" alt="07 Add roles and features" src="https://github.com/user-attachments/assets/315244ef-417c-4aa8-aeb8-f27b9a34007c" />


 Select **Active Directory Domain Services (AD DS)**.
- Proceed through the wizard and install.

![Screenshot 2025-05-22 121410](https://github.com/user-attachments/assets/917b1fc2-2975-4e5a-bb16-bbc428fd1307)

<img width="854" alt="10-ADDS Installed" src="https://github.com/user-attachments/assets/7e3f8743-d2d7-4160-b5ff-155f83dff5d1" />


### 6. **Promote to Domain Controller**
- After AD DS installation, choose "Promote this server to a domain controller".
<img width="842" alt="11-promote to DC" src="https://github.com/user-attachments/assets/9e4a5ea0-f0e9-4547-8a0a-3ff53e979e71" />

- Create a new forest (`oluwaseun.local`).
<img width="826" alt="12-Add a new forest" src="https://github.com/user-attachments/assets/f457ed2a-4835-4b9c-8a38-459ba853010e" />

- Set DSRM password and complete installation.

- <img width="857" alt="13  DSRM" src="https://github.com/user-attachments/assets/d1337576-b31b-4970-86f2-0fd2b34b6a21" />

- Restart the server.
![Screenshot 2025-05-22 130340](https://github.com/user-attachments/assets/4e88c935-e1a8-473e-9278-dd50c44da7f7)

<img width="833" alt="22-final setup" src="https://github.com/user-attachments/assets/e41b43a4-038f-4c91-9ccc-7b6b317b36bd" />



### 7. **Verify Configuration**
- Open `Active Directory Users and Computers`.

- <img width="956" alt="01-users and computers " src="https://github.com/user-attachments/assets/6d232150-17c6-4a2e-aaf5-1adc529c9040" />


- Create a user accounts to verify the domain functionality
<img width="836" alt="02-New_user" src="https://github.com/user-attachments/assets/652a6056-ebee-45a4-b034-10173dc870f6" />

<img width="362" alt="03-New-Object-User" src="https://github.com/user-attachments/assets/2bbf45f3-ee9b-4ea4-a156-8bfed5cf04c0" />

<img width="356" alt="04-User-Password" src="https://github.com/user-attachments/assets/e8516158-1e69-4df0-990f-206e78c56cff" />

<img width="848" alt="05-New-User" src="https://github.com/user-attachments/assets/690d19bd-3187-49a1-9c0b-637f684407c2" />


- Sign-in with the new user
<img width="824" alt="06-New-User-Signin" src="https://github.com/user-attachments/assets/f08809bf-3dc4-4790-9f9f-37ece76e77f1" />




---

## 🧠 Skills Learned

- Installing and configuring Windows Server 2025.
- Setting up and managing a virtual lab environment.
- Configuring static IPs and system roles.
- Installing and configuring Active Directory Domain Services.
- Promoting a server to a Domain Controller.
- Understanding basic networking and system administration tasks.

