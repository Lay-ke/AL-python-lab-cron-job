# Service Management and Temporary Folder Cleanup Script

## Overview

This Python script is designed to automate system maintenance tasks, specifically focusing on:

1. **Restarting a specified service** using `systemctl`.
2. **Clearing a specified temporary folder** to free up disk space.

The script is useful for system administrators who need to automate service management and cleanup tasks on Linux-based systems.

## Prerequisites

Make sure your system meets the following requirements:

- **Python 3.x** is installed.
- The script is run on a **Linux system** with `systemctl` support.
- User has **sudo privileges** to restart services.


## How It Works

The script performs two main operations:

1. **Restart a System Service**:
    - The `restart_service` function takes the name of a system service (e.g., `cron`) and attempts to restart it using `sudo systemctl restart <service_name>`.
    - If the service is restarted successfully, a confirmation message is printed.
    - If an error occurs during the restart, an error message is displayed.

2. **Clear a Temporary Folder**:
    - The `clear_temp_folder` function accepts a folder path, creates the folder if it doesn't exist, and then deletes it using `shutil.rmtree()`.
    - This is useful for clearing cache or temporary files.

## How to Run

1. Clone the repository or download the script.

2. Open a terminal and navigate to the directory containing the script.

3. Make the script executable (if necessary):

   ```bash
   chmod +x service_cleanup.py

4. Run the script with:

   ```bash
   sudo python3 service_cleanup.py

## Expected Output

   ```adruino
   Service 'cron' restarted successfully.
   Temporary folder '/home/yaw/temp_folder' cleared successfully.
