# Ubuntu Server Homelab

## Overview

Built an Ubuntu Server virtual machine using Oracle VirtualBox on a Windows host. Configured remote administration through SSH and deployed an Nginx web server.

## Objectives

- Learn virtualization and VM configuration.
- Install and update Ubuntu Server.
- Configure SSH for remote administration.
- Configure VirtualBox NAT port forwarding.
- Install and verify Nginx.
- Practice basic Linux service management and troubleshooting.

## Environment

| Component | Configuration |
|---|---|
| Host OS | Windows |
| Host CPU | Intel Core i5-11400F |
| Host RAM | 32 GB |
| Hypervisor | Oracle VirtualBox |
| Guest OS | Ubuntu Server LTS |
| VM RAM | 4 GB |
| VM CPUs | 2 |
| Virtual disk | 30 GB, dynamically allocated |
| Network | NAT |
| Remote access | OpenSSH |
| Web server | Nginx |

## Network Configuration

| Service | Host Port | Guest Port |
|---|---:|---:|
| SSH | 2222 | 22 |
| HTTP | 8080 | 80 |

The services are accessed locally from the Windows host.

## Implementation

1. Created the Ubuntu Server VM.
2. Installed Ubuntu Server and updated packages.
3. Installed and enabled OpenSSH.
4. Configured VirtualBox port forwarding for SSH.
5. Connected to Ubuntu from Windows PowerShell.
6. Installed and started Nginx.
7. Configured port forwarding to access the web server.
8. Verified the Nginx welcome page in a Windows browser.

## Validation

- SSH connection from Windows: Successful
- Nginx service status: Verified running
- Web page accessible at `http://127.0.0.1:8080`: Successful

## Troubleshooting Notes

### SSH connection refused

**Symptom:** PowerShell could not connect to `127.0.0.1` on port `2222`.

**Resolution:** Checked that the VM was running, verified the SSH service, and checked the VirtualBox NAT port-forwarding configuration. The SSH connection subsequently succeeded.

## Lessons Learned

- How virtual machines use host resources.
- How SSH enables remote Linux administration.
- How VirtualBox NAT port forwarding exposes selected guest services to the host.
- How to verify Linux services with `systemctl`.

## Next Steps

- Customize the Nginx homepage.
- Inspect Nginx access and error logs.
- Practice Linux users, groups, and file permissions.
- Document additional networking and system administration projects.

## Evidence

