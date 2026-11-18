# Ansible Final Project – Automation Roles

An academic automation project built for the BMCC CS-320 final project. It uses Ansible playbooks and roles to practice configuring Windows and Linux systems.

## What the project covers

### Linux automation
- **firewall_linux** – configures firewalld and manages web-service ports
- **nginx** – installs and configures an NGINX web server
- **freeradius** – sets up FreeRADIUS authentication
- **email_server** – explores Postfix/Dovecot mail-server configuration

### Windows automation
- **windows_security** – configures Windows Firewall and Windows Defender
- **bitlocker** – demonstrates BitLocker configuration
- **system_monitoring** – gathers CPU, memory, and disk information
- **windows_updates** – manages Windows updates and reboot handling
- **windows_software** – automates installation of selected applications

## Requirements

- Ansible installed on the control machine
- Reachable Linux and/or Windows test machines
- Appropriate SSH access for Linux hosts
- WinRM configured for Windows hosts
- A valid inventory file for your lab environment

## Configure the inventory

Create or edit the `hosts` inventory file with your own lab machine details. Example placeholders:

```ini
[linux]
192.0.2.10 ansible_user=YOUR_USER

[windows]
192.0.2.20 ansible_user=Administrator ansible_connection=winrm
```

Use your own secure authentication method and connection settings. Do not put real passwords, private keys, BitLocker recovery keys, tokens, or other secrets in this repository. Keep sensitive values outside version control (for example, with Ansible Vault or environment-specific secret management).

## Run the playbooks

Run the Linux and Windows playbooks separately:

```bash
ansible-playbook -i hosts linux.yml
ansible-playbook -i hosts windows.yml
```

Review each playbook and role before running it, and test in an isolated lab environment first.

## Learning goals

This project provided practice with:
- Ansible inventories, playbooks, and roles
- Linux service and firewall configuration
- Windows security and system administration tasks
- Repeatable automation and troubleshooting

## Project context

Academic lab project. The playbooks are intended for learning and testing, not as a production-ready deployment.
