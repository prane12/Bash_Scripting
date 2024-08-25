Real-Time System Monitoring Dashboard Script

Overview
This script provides a real-time monitoring dashboard for various system metrics, including CPU usage, memory usage, network activity, disk space, system load averages, active processes, and service status. It can be run continuously with a configurable refresh interval or specific parts can be called individually using command-line options.

Features

CPU Usage: Displays the top 10 applications consuming the most CPU.
Memory Usage: Displays the top 10 applications consuming the most memory.
Network Monitoring: Shows the number of concurrent connections, packet drops, and data transfer statistics.
Disk Space Usage: Lists disk usage by mounted partitions and partitions using more than 80% of the space.
System Load Averages: Displays the system's load averages.
CPU Usage Breakdown: Shows detailed CPU usage statistics.
Memory Usage Details: Displays detailed memory usage statistics.
Swap Memory Usage: Shows total, used, and free swap memory.
Active Processes: Lists the number of active processes and the top 5 by CPU and memory usage.
Service Monitoring: Checks the status of essential services like SSH, web server, and firewall services.

Prerequisites
The script is designed to run on Unix-like systems (Linux or macOS).
Ensure you have the necessary permissions to execute system commands like ps, ss, netstat, df, uptime, free, and systemctl.
