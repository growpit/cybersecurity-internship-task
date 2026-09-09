# Cybersecurity & Ethical Hacking Internship

**Intern:** Chandiswar Murmu
**Program:** ApexPlanet Software Pvt. Ltd. — Cybersecurity & Ethical Hacking Internship

## Task 1: Foundation & Environment Setup

This repository documents the setup of an isolated cybersecurity lab environment used throughout the internship.

### Environment
- **Hypervisor:** Oracle VirtualBox
- **Attacker Machine:** Kali Linux (192.168.56.102)
- **Target Machine:** Metasploitable2 (192.168.56.101)
- **Network:** Host-Only Adapter (isolated private lab network)

### What's in this repo
- [`lab-setup-notes.md`](./lab-setup-notes.md) — detailed notes on the lab setup process
- [`linux-cheatsheet.md`](./linux-cheatsheet.md) — reference of Linux commands used

### Summary
Kali Linux and Metasploitable2 were configured on an isolated Host-Only network, connectivity was verified via `ping`, and traffic was captured and analyzed using Wireshark. This lab forms the foundation for the network scanning, web application security, and exploitation tasks later in the internship.
