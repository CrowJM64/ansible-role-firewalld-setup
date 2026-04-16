# Ansible Role for FirewallD Setup and UFW removal
**Author/Maintainer:** Josh Murphy

## Overview

This Ansible role installs FirewallD and removes UFW, adding SSH to the allowlist, along with any other ports you need.
```yaml
- Removes UFW if applicable
- Installs python3-firewall on Debian. (Required for Ansible FW Management on Debian)
- Ensures FirewallD is both installed and up to date.
- Allows the requested ports.
- Allows the requested services.
- Ensures FirewallD is enabled and restarts it.
```

## Dependencies
- ansible.posix

## Supported Platforms and Derivatives
This playbook should work on most Redhat and Debian Distributions. Below are the explicitly tested Distros:
```yaml
# RedHat
Rocky 10/9
CentOS 10/9
Fedora 43/42
Oracle 10

# Debian
Ubuntu 24.04/22.04
Debian 13
Alma 10
Mint 22
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