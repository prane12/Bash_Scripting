## Real-Time System Monitoring Dashboard Script

### **Overview**
This script provides a real-time monitoring dashboard for various system metrics, including CPU usage, memory usage, network activity, disk space, system load averages, active processes, and service status. It can be run continuously with a configurable refresh interval or specific parts can be called individually using command-line options.

 ### **Features**

-  **CPU Usage**: Displays the top 10 applications consuming the most CPU.

-  **Memory Usage**: Displays the top 10 applications consuming the most memory.
  
-  **Network Monitoring**: Shows the number of concurrent connections, packet drops, and data transfer statistics.

-  **Disk Space Usage**: Lists disk usage by mounted partitions and partitions using more than 80% of the space.

-  **System Load Averages**: Displays the system's load averages.

-  **CPU Usage Breakdown**: Shows detailed CPU usage statistics.

-  **Memory Usage Details**: Displays detailed memory usage statistics.

-  **Swap Memory Usage**: Shows total, used, and free swap memory.

-  **Active Processes**: Lists the number of active processes and the top 5 by CPU and memory usage.

-  **Service Monitoring**: Checks the status of essential services like SSH, web server, and firewall services.

### **Prerequisites**
The script is designed to run on Unix-like systems (Linux or macOS).
Ensure you have the necessary permissions to execute system commands like **ps**, **ss**, **netstat**, **df**, **uptime**, **free**, and **systemctl**.

### Installation
Clone the repository or download the script file.
Make the script executable:

`chmod +x dashboard.sh`

### Usage
You can run the script in various modes depending on the monitoring data you wish to see. Below are the options available:


### Options

- `-c`: **Show top 10 applications by CPU usage.**
- `-m`: **Show top 10 applications by memory usage.**
- `-n`: **Show network monitoring information.**
- `-d`: **Show disk space usage by mounted partitions.**
- `-l`: **Show system load averages.**
- `-u`: **Show CPU usage breakdown and memory usage.**
- `-s`: **Monitor essential services** (e.g., SSH, web server, firewall).
- `-a`: **Show the number of active processes** and the top 5 processes by CPU and memory usage.


### Examples
Run the script with a full dashboard:

`./dashboard.sh`

This will run all the monitoring functions in a loop with the default refresh interval.

### Run the script to display CPU usage only:

`./dashboard.sh -c`

### Display memory usage and network monitoring information:

`./dashboard.sh -m -n`

### Monitor essential services like SSH and web servers:

`./dashboard.sh -s`

### Show CPU and memory usage details:

`./dashboard.sh -u`

### Configuring the Refresh Interval
To change the refresh interval, modify the REFRESH_INTERVAL variable at the top of the script:

`REFRESH_INTERVAL=10`








## Security Audit and Hardening Script

### Overview
This bash script performs a comprehensive security audit and hardening of a Linux server. It checks various system configurations, permissions, and services to identify potential security issues and ensure best practices. The script also includes functions for configuring SSH, disabling IPv6, securing the GRUB bootloader, and more.

### Features
### User and Group Audits: 
Lists all users and groups, checks for users with root privileges, and identifies users without passwords.

### File and Directory Permission Audits:
Finds files and directories with world-writable permissions, and checks permissions on .ssh directories.

### Service Checks:
Identifies unnecessary services running, verifies critical services, and checks for services listening on non-standard ports.

### Firewall Configuration:
Verifies and configures firewall settings with UFW or iptables.

### Network Security:
Checks IP forwarding and the type of IP addresses (public/private).

### Failed Login Attempts: 
Reports and alerts on failed login attempts.

### Server Hardening: 
Configures SSH, disables IPv6, secures GRUB bootloader, and sets up unattended-upgrades.

### Report Generation:
Creates a summary report of the audit and hardening steps, with optional email alerts for warnings.

## Prerequisites

### Root Privileges:
The script must be run as root or with sudo privileges.

## Dependencies:
mail command (for email alerts), unattended-upgrades, iptables or ufw.

## Usage
Ensure you have root privileges:


