# README
## Design and Implementation of Secure FTP Server using SFTP

**Students:** Uzair Ahmad(BSIT-023R22P-9) and Abdullah Majeed(BSIT-023R22P-28)  
**Department:** Computer Science / Information Technology  
**Institution:** University of Southern Punjab, Multan

---

## 1. Project Title and Description

**Project Title:** Design and Implementation of Secure FTP Server using SFTP

This project implements a secure file transfer system using the Secure File Transfer Protocol (SFTP) over SSH. The system uses OpenSSH Server on Windows and WinSCP as the client application.

The purpose of the project is to provide secure file transfer between a client and server over a network. The system supports authenticated access and user-specific access restrictions according to the server configuration.

The project demonstrates SSH service configuration, firewall configuration, user authentication, SFTP connectivity, and secure file transfer testing.

## 2. Tools, Technologies, and Software Used

The following tools and technologies are used in this project:

- **Operating System:** Windows
- **SSH Server:** OpenSSH Server
- **File Transfer Protocol:** SFTP over SSH
- **Client Application:** WinSCP
- **Configuration File:** `sshd_config`
- **Command-Line Tool:** Windows PowerShell
- **Network Protocol:** TCP/IP
- **Default SSH/SFTP Port:** TCP 22

## 3. System Requirements and Prerequisites

The following requirements are needed to set up and test the project:

- A Windows computer configured as the SFTP server.
- OpenSSH Server installed and configured on the server.
- A client computer with WinSCP installed, or another compatible SFTP client.
- A working network connection between the server and client.
- TCP port 22 permitted through the appropriate firewall.
- Valid Windows user accounts and configured authentication.
- Correct directory permissions and user access restrictions.

**Project network details:**

- Server IP address: `192.168.10.11`
- Client IP address: `192.168.10.7`
- SSH/SFTP port: `22`
- SSH service name: `sshd`
- SSH configuration path: `C:\ProgramData\ssh\sshd_config`

The IP addresses above are the local network addresses used during project testing. They may need to be changed if the project is deployed on another network.

## 4. Installation and Configuration Instructions

### Step 1: Prepare the Windows Server

Use a Windows computer as the server and connect it to the required network.

### Step 2: Install OpenSSH Server

Install the OpenSSH Server Windows capability if it is not already installed. Verify its installation before proceeding.

### Step 3: Configure the SSH Service

Ensure that the `sshd` service is running. Configure the service to start automatically if required.

### Step 4: Configure the Firewall

Allow incoming TCP connections on port 22 through Windows Firewall when required. Check existing firewall rules before creating additional rules.

### Step 5: Configure SSH/SFTP Settings

Open the configuration file:

`C:\ProgramData\ssh\sshd_config`

Review the settings for authentication, SFTP access, and user-specific restrictions. Apply only the settings appropriate to the final project configuration.

### Step 6: Configure User Accounts and Directories

Create or verify the required Windows user accounts and SFTP directories. Configure permissions so that users can access only the directories and operations permitted by the final configuration.

### Step 7: Apply Configuration Changes

Validate the configuration and restart the SSH service when necessary. Confirm that the service starts successfully.

### Step 8: Configure the Client

Install WinSCP on the client computer and prepare an SFTP connection using the server IP address, port, username, and configured authentication method.

## 5. Dependencies and Their Installation

This project uses Windows OpenSSH Server and WinSCP rather than a separate custom application.

**Required components:**

1. **OpenSSH Server:** Provides the SSH service and SFTP functionality on the server.
2. **WinSCP:** Provides a graphical interface for connecting to the SFTP server and transferring files.
3. **Windows PowerShell:** Used to inspect services, network settings, firewall rules, and configuration.
4. **Windows Firewall:** Controls incoming network access to the server.

Install OpenSSH Server through Windows Optional Features or the supported Windows installation method. Install WinSCP on the client computer using its official installer.

No separate programming-language packages or third-party application libraries are required for the basic OpenSSH and WinSCP setup.

## 6. Database and Dataset Setup

This project does not require a separate application database or a formal dataset.

OpenSSH Server manages the secure connection and file-transfer service. Files used during testing serve as sample test files for verifying upload and download functionality.

If sample files are included with the submission, they may be used to test file transfers between the client and server.

## 7. Instructions for Running the Project

### Step 1: Start the Server

Turn on the server computer and ensure that the OpenSSH `sshd` service is running.

### Step 2: Verify Network Connectivity

Check the server IP address and confirm that the client can reach the server over the network.

### Step 3: Verify Port 22

Ensure that TCP port 22 is permitted by the firewall and that the SSH service is listening for connections.

### Step 4: Open WinSCP

Launch WinSCP on the client computer.

### Step 5: Enter Connection Details

Select **SFTP** as the file protocol and enter:

- **Host name:** `192.168.10.11`
- **Port number:** `22`
- **User name:** A configured project user account
- **Password or private key:** Use the authentication method configured for that account.

### Step 6: Connect to the Server

Connect using the configured account and accept the server host key only after verifying it when possible.

### Step 7: Test File Transfer

Upload a sample file from the client to an authorized server directory. Download a permitted file back to the client to verify file-transfer functionality.

### Step 8: Verify Access Restrictions

Test whether each user can access the permitted directory and whether restricted locations or operations are denied according to the final configuration.

### Step 9: Confirm Successful Operation

Record the actual results of connection, upload, download, authentication, and access-restriction tests.

## 8. Troubleshooting

- **Connection refused:** Check whether the `sshd` service is running.
- **Connection timeout:** Check the server IP, network connectivity, and firewall rules.
- **Authentication failure:** Verify the username and the configured authentication method.
- **Permission denied:** Review Windows folder permissions and the SSH/SFTP configuration.
- **Incorrect directory access:** Review the user-specific configuration and directory restrictions.
- **Configuration error:** Review `sshd_config` before restarting the SSH service.

## 9. Supporting Files

The project submission may include the final report, PowerShell command documentation, relevant configuration files, and sample test files where applicable.

Any configuration file included in the submission should correspond to the final tested setup. Do not include passwords or private SSH keys.

## 10. Conclusion

The project demonstrates the configuration and testing of a secure file-transfer service using OpenSSH Server and SFTP. WinSCP is used as the client for connecting to the server and transferring files. The security and access restrictions depend on the final verified server configuration.

