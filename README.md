# Ansible Role for FirewallD Setup and UFW removal
**Author/Maintainer:** Josh Murphy

## Overview

This Ansible role installs FirewallD and removes UFW, adding SSH to the allowlist, along with any other ports you need.
```yaml
- Removes UFW if applicable
- Ensures FirewallD is installed and up to date.
- Allows the SSH service.
- Allows any other desired ports.
- Restarts FirewallD
```

## Supported Platforms and Derivatives
These changes should work on every Redhat and Debian Distro. Below are the explicitly supported Distros.
```yaml
# RedHat
EL - All Versions
Fedora - All Versions
Rocky - All Versions
AlmaLinux - All Versions

# Debian
Debian - All Versions
Ubuntu - All Versions
```

## Example Playbook

```yaml
- hosts: all
  become: yes

  roles:
    - role: firewalld_setup
```

### From Ansible Galaxy

```bash
ansible-galaxy install crowjm64.firewalld_setup
```

This role was created and is maintained by **[CrowJM64](https://github.com/CrowJM64)**.