# Kaminski Common Ansible Collection

This repository contains shared Ansible roles.

## Collection: kaminski.common

### Roles

#### 1. system_update
Manages OS-specific system updates and cleanup.
- **Supported OS**: Ubuntu, Debian, Raspbian, Fedora.
- **Variables**:
  - `perform_system_update`: (Boolean) Set to `true` to execute updates (Default: `false`).

#### 2. users_ssh
Manages user accounts, groups, and SSH authorized keys following a managed pattern.
- **Variables**:
  - `managed_groups`: Dictionary of groups with GIDs.
  - `managed_users`: Dictionary of users with UIDs, groups, and shells.
  - `managed_ssh_keys`: List of SSH keys per user.
  - `ssh_password_authentication`: (Boolean) Enable/disable password auth (Default: `false`).
  - `ssh_pubkey_authentication`: (Boolean) Enable/disable pubkey auth (Default: `true`).
  - `manage_ssh_config`: (Boolean) Whether to enforce SSH hardening (Default: `false`).

## Installation

Add to your `requirements.yml`:

```yaml
collections:
  - name: kaminski.common
    source: https://github.com/nkaminski/ansible-common.git
    type: git
    version: 1.0.0
```
