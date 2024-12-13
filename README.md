# README - Linux Basics and System Administration

This document provides an overview of essential Linux concepts and tools.

---

## 1. Virtualization

**Virtualization** allows running multiple operating systems on a single physical machine. Tools like VirtualBox, VMware, and KVM enable efficient resource utilization and testing environments.

---

## 2. Partitions

**Partitions** divide a disk into separate sections for better organization and isolation. Common types include primary, extended, and logical partitions. Efficient partitioning ensures optimized performance and data safety.

---

## 3. AppArmor

**AppArmor** is a Linux security module that restricts applications' capabilities through profiles, enhancing the system's security. It is particularly useful for isolating vulnerable or high-risk applications.

---

## 4. LVM (Logical Volume Manager)

**LVM** provides flexible disk management by allowing resizing and creating logical volumes without unmounting partitions. This makes it easier to adapt to changing storage needs.

---

## 5. sudo vs su

- **sudo:** Executes commands with elevated privileges temporarily, ensuring security by not sharing the root password.
- **su:** Switches to another user account, often root, requiring its password. It provides full root access but can pose security risks if misused.

---

## 6. SSH (Secure Shell)

**SSH** allows secure remote access and management of servers. Use public/private key pairs for enhanced security, and disable password-based authentication where possible.

---

## 7. User Management

Tools like `adduser`, `deluser`, and `usermod` manage system users and groups effectively. Proper user management ensures controlled access and system integrity.

---

## 8. Password Policies

Implement strong password policies using `passwd` and configure password expiration and complexity requirements in `/etc/login.defs`. Use tools like `faillog` to monitor failed login attempts.

---

## 9. UFW (Uncomplicated Firewall)

**UFW** simplifies managing iptables, enabling you to allow, deny, or limit network traffic with commands like `ufw allow 22`. Always ensure unnecessary ports are closed to minimize vulnerabilities.

---

## 10. Crontab

**Crontab** schedules recurring tasks. Example: `0 2 * * * /path/to/script.sh` runs a script daily at 2 AM. Use `crontab -e` to edit jobs and `crontab -l` to list current jobs.

---

## 11. Why Debian?

**Debian** is known for stability, extensive package repositories, and community support. It is an excellent choice for servers and desktops due to its robust performance and free software philosophy.

---

## 12. Debian vs Rocky

- **Debian:** Focuses on stability and freedom, making it ideal for general-purpose use and development.
- **Rocky:** An enterprise Linux distribution compatible with Red Hat, designed for business environments requiring long-term support.

---

## 13. Hostname and Networking

Use `hostnamectl` to set or view the hostname. Configure network settings in `/etc/network/interfaces` or use tools like `nmcli`. Regularly monitor network configurations to ensure stability.

---

## 14. Basic Bash Commands

- `ls`: List files and directories
- `cd`: Change directory
- `grep`: Search text in files
- `find`: Locate files
- `top`: Monitor system processes
- `df -h`: Display disk space usage
- `free -m`: Check memory usage

---

## 15. Monitoring with monitoring.sh

Create a script like `monitoring.sh` to log system metrics such as CPU and memory usage. Example:

```bash
#!/bin/bash
while true; do
    echo "CPU: $(top -bn1 | grep 'Cpu(s)' | awk '{print $2}')%" >> /var/log/monitor.log
    echo "Memory: $(free -m | awk '/Mem:/ {print $3}')MB" >> /var/log/monitor.log
    sleep 60
done
```

---

## 16. apt vs aptitude

- **apt:** A command-line tool for package management, widely used and simple to use.
- **aptitude:** Offers a text-based UI with enhanced dependency resolution, useful for advanced users.

---

## Author

Created by **Abderrahmane Sebban**

