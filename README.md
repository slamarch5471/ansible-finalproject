# Ansible Final Project – Automation Roles

This repository contains a collection of Ansible roles and playbooks designed to automate the deployment and configuration of Windows and Linux machines.  
This project was built for the BMCC CS-320 Final Project.

---

## 📌 Project Contents

### 🖥️ Linux Automation
- **firewall_linux**: Configures firewalld and opens ports (80, 443)
- **nginx**: Installs and configures an NGINX web server
- **freeradius**: Installs, configures, and sets up FreeRADIUS authentication
- **email_server**: Installs and configures Postfix/Dovecot (if used)

### 🪟 Windows Automation
- **windows_security**: Configures Windows Firewall and Windows Defender
- **bitlocker**: Enables BitLocker disk encryption and generates recovery keys
- **system_monitoring**: Gathers CPU, RAM, and disk usage
- **windows_updates**: Installs Windows Updates and reboots if necessary
- **windows_software**: Installs Chrome, Firefox, VLC, and Office

---

## 🚀 How to Run the Project

### 1. Update the inventory (hosts) file

[linux]IP ADDRESS ansible_user=USERNAME ansible_password=YOURPASS ansible_become_password=YOURPASS

[windows]
IP ADDRESS ansible_user=Administrator ansible_password=YOURPASS ansible_connection=winrm

### 2. Run ALL roles using the master playbook:

ansible-playbook -i hosts linux.yml
ansible-playbook -i hosts windows.yml

