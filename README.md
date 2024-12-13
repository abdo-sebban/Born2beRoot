<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <header>
        <h1>README - Linux Basics and System Administration</h1>
        <p>This document provides an overview of essential Linux concepts and tools.</p>
    </header>
    <main>
        <section>
            <h2>1. Virtualization</h2>
            <p>Virtualization allows running multiple operating systems on a single physical machine. Tools like VirtualBox, VMware, and KVM enable efficient resource utilization and testing environments.</p>
        </section>
        <section>
            <h2>2. Partitions</h2>
            <p>Partitions divide a disk into separate sections for better organization and isolation. Common types include primary, extended, and logical partitions.</p>
        </section>
        <section>
            <h2>3. AppArmor</h2>
            <p>AppArmor is a Linux security module that restricts applications' capabilities through profiles, enhancing the system's security.</p>
        </section>
        <section>
            <h2>4. LVM (Logical Volume Manager)</h2>
            <p>LVM provides flexible disk management by allowing resizing and creating logical volumes without unmounting partitions.</p>
        </section>
        <section>
            <h2>5. sudo vs su</h2>
            <p>
                <strong>sudo:</strong> Executes commands with elevated privileges temporarily.
                <br>
                <strong>su:</strong> Switches to another user account, often root, requiring its password.
            </p>
        </section>
        <section>
            <h2>6. SSH (Secure Shell)</h2>
            <p>SSH allows secure remote access and management of servers. Use public/private key pairs for enhanced security.</p>
        </section>
        <section>
            <h2>7. User Management</h2>
            <p>Tools like <code>adduser</code>, <code>deluser</code>, and <code>usermod</code> manage system users and groups effectively.</p>
        </section>
        <section>
            <h2>8. Password Policies</h2>
            <p>Implement strong password policies using <code>passwd</code> and configure password expiration and complexity requirements in <code>/etc/login.defs</code>.</p>
        </section>
        <section>
            <h2>9. UFW (Uncomplicated Firewall)</h2>
            <p>UFW simplifies managing iptables, enabling you to allow, deny, or limit network traffic with commands like <code>ufw allow 22</code>.</p>
        </section>
        <section>
            <h2>10. Crontab</h2>
            <p>Crontab schedules recurring tasks. Example: <code>0 2 * * * /path/to/script.sh</code> runs a script daily at 2 AM.</p>
        </section>
        <section>
            <h2>11. Why Debian?</h2>
            <p>Debian is known for stability, extensive package repositories, and community support. It is an excellent choice for servers and desktops.</p>
        </section>
        <section>
            <h2>12. Debian vs Rocky</h2>
            <p>
                Debian focuses on stability and freedom, while Rocky is an enterprise Linux distribution compatible with Red Hat, designed for business environments.
            </p>
        </section>
        <section>
            <h2>13. Hostname and Networking</h2>
            <p>Use <code>hostnamectl</code> to set or view the hostname. Configure network settings in <code>/etc/network/interfaces</code> or use tools like <code>nmcli</code>.</p>
        </section>
        <section>
            <h2>14. Basic Bash Commands</h2>
            <ul>
                <li><code>ls</code>: List files and directories</li>
                <li><code>cd</code>: Change directory</li>
                <li><code>grep</code>: Search text in files</li>
                <li><code>find</code>: Locate files</li>
                <li><code>top</code>: Monitor system processes</li>
            </ul>
        </section>
        <section>
            <h2>15. Monitoring with monitoring.sh</h2>
            <p>Create a script like <code>monitoring.sh</code> to log system metrics such as CPU and memory usage.</p>
        </section>
        <section>
            <h2>16. apt vs aptitude</h2>
            <p>
                <strong>apt:</strong> A command-line tool for package management.
                <br>
                <strong>aptitude:</strong> Offers a text-based UI with enhanced dependency resolution.
            </p>
        </section>
    </main>
    <footer>
        <p>Created by Abderrahmane Sebban | <a href="https://github.com/abdo-sebban">GitHub Profile</a></p>
    </footer>
</body>
</html>
