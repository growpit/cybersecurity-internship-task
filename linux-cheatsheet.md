# Linux Cheat-Sheet — Cybersecurity Internship (Task 1)

## File System Navigation
- `pwd` — print current directory
- `ls` — list files
- `ls -la` — list all files with details, including hidden ones
- `cd <folder>` — change directory
- `cd ..` — go up one directory

## File & Directory Permissions
- `chmod +x file` — make a file executable
- `chmod 755 file` — set specific permission bits
- `chown user:group file` — change file owner

## Package Management
- `sudo apt update` — refresh package list
- `sudo apt install <package>` — install a package
- `dpkg -l` — list installed packages

## Networking Commands
- `ip addr show eth0` — show IP address of interface
- `ping -c 4 <ip>` — send 4 ping packets to test connectivity
- `netstat -tulnp` — show open ports and listening services
- `traceroute <ip>` — trace the network path to a host

## Other Useful Commands
- `sudo poweroff` — shut down the machine safely
- `whoami` — show current logged-in user
- `history` — show command history
