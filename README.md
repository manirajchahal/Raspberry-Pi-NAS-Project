# Raspberry-Pi-NAS-Project

# Personal NAS Build with Raspberry Pi 5

## Overview
I built this personal NAS using a Raspberry Pi 5 and a Toshiba 2 TB hard drive to create a centralized, secure, and energy-efficient storage solution. This project allowed me to explore hardware integration, Linux system administration, and network configuration while establishing a robust platform for file management, media streaming, and remote access.

## Features
- **Centralized Data Management:** Store and access all files from one location.
- **Secure Remote Access:** Retrieve and share files securely from anywhere.
- **Enhanced Data Security:** Utilize encryption and regular backup protocols.
- **Cost-Effective:** A budget-friendly alternative to cloud storage with scalable options.
- **Energy Efficiency:** Low-power hardware ensures an environmentally friendly setup.

## Hardware Components
- **Raspberry Pi 5**
- **Toshiba 2 TB Hard Drive**
- Additional items: Power supply, microSD card, cables, and necessary adapters.

## Software & Technologies
- **Operating System:** Raspberry Pi OS (or any preferred Linux distribution)
- **File Sharing:** Samba
- **Networking:** Secure file sharing protocols and remote access configuration

## Installation & Setup
1. **Hardware Assembly:**  
   - Connect the Toshiba 2 TB hard drive to the Raspberry Pi 5.
   - Ensure all components are powered correctly.

2. **OS Installation:**  
   - Install Raspberry Pi OS on your Raspberry Pi.
   - Update the system and install required packages:
     ```bash
     sudo apt-get update && sudo apt-get upgrade
     sudo apt-get install samba samba-common
     ```

3. **Configuration:**  
   - Configure Samba or your preferred file-sharing service by editing the configuration file (e.g., /etc/samba/smb.conf). 
     ```bash
     [MyMedia] path = /media/pi/MyExternalDrive/ 
     writeable = yes
     create mask = 0775 
     directory mask = 0775 
     public=no 
     ```
   - Set up necessary permissions and security measures (e.g. user authentication).

4. **Testing & Deployment:**  
   - Test remote access and file-sharing capabilities from another device.

## Usage
- **Data Management:** Easily store, organize, and backup your data.
- **Remote Access:** Access your files from any networked device securely.
- **Media Streaming:** Enjoy media directly from your NAS with compatible applications.
- **Automation:** Leverage custom scripts to automate routine tasks like backups and monitoring.

## License
This project is licensed under the MIT License.
