# Coffre - A Distributed System for Secure Programming Labs

Coffre (French for "vault") is a specialized virtual environment system designed to prevent code sharing and copying during programming assignments. It was developed at IIT Bombay as a Bachelor's Thesis project under Prof. Uday Khedker.

## Key Features

- **Isolated Environment**: Students work in a secure virtual machine environment that prevents copying files in/out or accessing the internet
- **Distributed Access**: Students can access their environment from any system while maintaining security
- **Built-in Version Control**: Each student/group gets a private Git repository to sync work between multiple instances
- **Secure Submissions**: Built-in submission system for assignments that maintains integrity and prevents tampering
- **Full Disk Encryption**: Uses encrypted virtual disk images with network-based key management
- **Granular Access Control**: Fine-grained permissions system for students, TAs, and professors

## Core Security Features

- No copy-paste between host and guest OS
- No external media mounting (USB, CD/DVD)
- No internet access except to allowed servers
- SSH key-based authentication with hardened configuration
- Custom SSH binaries with embedded credentials
- GRUB security to prevent recovery mode access
- Encrypted disk images with Mandos-based key management

## Architecture

- **Client**: Ubuntu-based virtual machine images running in VirtualBox
- **Server Components**:
  - Git server for private repositories (using Gitosis)
  - Submission server for assignments
  - Django web server for professor interface
  - Mandos server for disk encryption keys

## Usage

Students receive:
1. Base VDI (Virtual Disk Image) file
2. Group credentials for setup
3. Instructions for VirtualBox configuration

The system provides:
- Terminal-based submission client
- Git for version control
- Automatic updates mechanism
- TA interface for managing submissions

## Development Team

- Vamsi Bedapudi (150050068)
- Bhavan Turaka (150050091)
- Under supervision of Prof. Uday Khedker

## Documentation

For detailed setup and usage instructions, see:
- User Manual & FAQs
- Professor Manual
- Admin Manual 
- Technical Documentation

## Note

This system was designed specifically for programming lab courses at IIT Bombay. While the code is being made public for demonstration purposes, it includes specific security features tied to the institute's infrastructure.

## Original Paper

This is the implementation of research work documented in "Coffre - A Distributed System for In & Out Labs" (2019) from the Department of Computer Science and Engineering, IIT Bombay.
