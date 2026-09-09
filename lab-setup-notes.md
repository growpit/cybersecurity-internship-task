# Lab Setup Notes — Task 1: Foundation & Environment Setup

## Environment
- Hypervisor: Oracle VirtualBox
- Attacker Machine: Kali Linux (Rolling)
- Target Machine: Metasploitable2 (deliberately vulnerable Ubuntu-based VM)

## Network Configuration
- Both VMs configured with a **Host-Only Adapter** (VirtualBox Host-Only Ethernet Adapter)
- This isolates the lab from the host machine's real network while still letting Kali and Metasploitable2 talk to each other
- Kali IP: 192.168.56.102
- Metasploitable2 IP: 192.168.56.101

## Steps Taken
1. Installed Oracle VirtualBox on the host machine.
2. Downloaded Metasploitable2 and imported the .vmdk disk into a new VM.
3. Set both Kali and Metasploitable2 network adapters to Host-Only mode so they share a private subnet.
4. Logged into Metasploitable2 with default credentials (msfadmin/msfadmin) and confirmed its IP with `ip addr show eth0`.
5. Booted Kali Linux and opened a terminal.
6. Ran `ping -c 4 192.168.56.101` from Kali — got 0% packet loss, confirming connectivity.
7. Opened Wireshark on Kali, started a live capture on eth0, generated ICMP traffic via ping, and confirmed the request/reply packets were visible along with ARP and DHCP traffic.

## Key Learnings
- Host-Only networking is the safest way to build an isolated pentesting lab — no risk to the real network.
- `ip addr show <interface>` is the modern replacement for `ifconfig` on newer Kali/Debian systems.
- Wireshark confirms not just connectivity but the actual packet structure (Ethernet, IP, ICMP headers) traveling between machines.

## Deliverables
- Lab Setup Report (Word doc) with screenshots of Kali, Metasploitable2, ping test, and Wireshark capture
- This GitHub repo with notes and Linux cheat-sheet
- 5-minute video walkthrough of the lab setup
