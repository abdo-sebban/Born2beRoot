<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README - Linux Basics</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0 20px;
        }
        header {
            background: #4CAF50;
            color: white;
            padding: 20px 10px;
            text-align: center;
            border-radius: 5px;
        }
        section {
            margin: 20px 0;
            padding: 15px;
            background: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        h2 {
            color: #4CAF50;
        }
        pre {
            background: #f9f9f9;
            border-left: 5px solid #4CAF50;
            padding: 10px;
            overflow-x: auto;
            font-size: 14px;
        }
        code {
            background: #eee;
            padding: 2px 5px;
            border-radius: 3px;
        }
        footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            background: #4CAF50;
            color: white;
            border-radius: 5px;
        }
        ul {
            padding-left: 20px;
        }
        ul li {
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <header>
        <h1>README - Linux Basics and System Administration</h1>
        <p>This document provides an overview of essential Linux concepts and tools.</p>
    </header>
    <main>
        <section>
            <h2>1. Virtualization</h2>
            <p><strong>Virtualization</strong> allows running multiple operating systems on a single physical machine. Tools like VirtualBox, VMware, and KVM enable efficient resource utilization and testing environments.</p>
        </section>
        <section>
            <h2>2. Partitions</h2>
            <p><strong>Partitions</strong> divide a disk into separate sections for better organization and isolation. Common types include primary, extended, and logical partitions. Efficient partitioning ensures optimized performance and data safety.</p>
        </section>
        <section>
            <h2>3. AppArmor</h2>
            <p><strong>AppArmor</strong> is a Linux security module that restricts applications' capabilities through profiles, enhancing the system's security. It is particularly useful for isolating vulnerable or high-risk applications.</p>
        </section>
        <section>
            <h2>4. LVM (Logical Volume Manager)</h2>
            <p><strong>LVM</strong> provides flexible disk management by allowing resizing and creating logical volumes without unmounting partitions. This makes it easier to adapt to changing storage needs.</p>
        </section>
        <section>
            <h2>5. sudo vs su</h2>
            <p>
                <strong>sudo:</strong> Executes commands with elevated privileges temporarily, ensuring security by not sharing the root password.
                <br>
                <strong>su:</strong> Switches to another user account, often root, requiring its password. It provides full root access but can pose security risks if misused.
            </p>
        </section>
        <section>
            <h2>6. SSH (Secure Shell)</h2>
            <p><strong>SSH</strong> allows secure remote access and management of servers. Use public/private key pairs for enhanced security, and disable password-based authentication where possible.</p>
        </section>
        <section>
            <h2>7. User Management</h2>
            <p>Tools like <code>adduser</code>, <code>deluser</code>, and <code>usermod</code> manage system users and groups effectively. Proper user management ensures controlled access and system integrity.</p>
        </section>
        <section>
            <h2>8. Password Policies</h2>
            <p>Implement strong password policies using <code>passwd</code> and configure password expiration and complexity requirements in <code>/etc/login.defs</code>. Use tools like <code>faillog</code> to monitor failed login attempts.</p>
        </section>
        <section>
            <h2>9. UFW (Uncomplicated Firewall)</h2>
            <p><strong>UFW</strong> simplifies managing iptables, enabling you to allow, deny, or limit network traffic with commands like <code>ufw allow 22</code>. Always ensure unnecessary ports are closed to minimize vulnerabilities.</p>
        </section>
        <section>
            <h2>10. Crontab</h2>
            <p><strong>Crontab</strong> schedules recurring tasks. Example: <code>0 2 * * * /path/to/script.sh</code> runs a script daily at 2 AM. Use <code>crontab -e</code> to edit jobs and <code>crontab -l</code> to list current jobs.</p>
        </section>
        <section>
            <h2>11. Why Debian?</h2>
            <p><strong>Debian</strong> is known for stability, extensive package repositories, and community support. It is an excellent choice for servers and desktops due to its robust performance and free software philosophy.</p>
        </section>
        <section>
            <h2>12. Debian vs Rocky</h2>
            <p>
                <strong>Debian</strong> focuses on stability and freedom, making it ideal for general-purpose use and development.
                <br>
                <strong>Rocky</strong> is an enterprise Linux distribution compatible with Red Hat, designed for business environments requiring long-term support.
            </p>
        </section>
        <section>
            <h2>13. Hostname and Networking</h2>
            <p>Use <code>hostnamectl</code> to set or view the hostname. Configure network settings in <code>/etc/network/interfaces</code> or use tools like <code>nmcli</code>. Regularly monitor network configurations to ensure stability.</p>
        </section>
        <section>
            <h2>14. Basic Bash Commands</h2>
            <ul>
                <li><code>ls</code>: List files and directories</li>
                <li><code>cd</code>: Change directory</li>
                <li><code>grep</code>: Search text in files</li>
                <li><code>find</code>: Locate files</li>
                <li><code>top</code>: Monitor system processes</li>
                <li><code>df -h</code>: Display disk space usage</li>
                <li><code>free -m</code>: Check memory usage</li>
            </ul>
        </section>
        <section>
            <h2>15. Monitoring with monitoring.sh</h2>
            <p>Create a script like <code>monitoring.sh</code> to log system metrics such as CPU and memory usage. Example:</p>
            <pre><code>#!/bin/bash
while true; do
    echo "CPU: $(top -bn1 | grep 'Cpu(s)' | awk '{print $2}')%" >> /var/log/monitor.log
    echo "Memory: $(free -m | awk '/Mem:/ {print $3}')MB" >> /var/log/monitor.log
    sleep 60
done
            </code></pre>
        </section>
        <section>
            <h2>16. apt vs aptitude</h2>
            <p>
                <strong>apt:</strong> A command-line tool for package management, widely used and simple to use.
                <br>
                <strong>aptitude:</strong> Offers a text-based UI with enhanced dependency resolution, useful for advanced users.
            </p>
        </section>
    </main>
    <footer>
        <p>Created by <strong>Abderrahmane Sebban</strong> | <a href="https://github.com">GitHub Profile</a></p>
    </footer>
</body>
</html>
