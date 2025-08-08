# UFW Firewall Configuration - Cybersecurity Internship Task

## Objective
Configure and test basic firewall rules using UFW (Uncomplicated Firewall) on Kali Linux.

## Commands Used

# 1. Update package list and install UFW
sudo apt update
sudo apt install ufw -y

# 2. Enable UFW
sudo ufw enable

# 3. Check UFW status
sudo ufw status verbose

# 4. Allow SSH (Port 22)
sudo ufw allow 22/tcp

# 5. Block Telnet (Port 23)
sudo ufw deny 23

# 6. List current firewall rules
sudo ufw status numbered

# 7. Test the rule using Telnet (install if not available)
sudo apt install telnet
telnet localhost 23

# 8. Remove the test block rule to restore original state
sudo ufw delete deny 23

# 9. Disable UFW if needed
sudo ufw disable

## Summary

These commands demonstrate how to:
- Set up UFW
- Allow and deny specific ports
- Test blocked ports using Telnet
- Manage and remove rules safely

## Notes
- Port 23 (Telnet) is blocked as it's an insecure protocol.
- Always allow SSH (port 22) before applying new firewall rules, especially on remote machines.

## Deliverables
- Screenshot of `ufw status numbered`
- Screenshot of Telnet test on port 23
