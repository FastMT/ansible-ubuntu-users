# ansible-ubuntu-users
Ansible template to manage local users on Ubuntu

## Installation

Create requirements.yml file

```
# Include ansible-ubuntu-users role
- src: https://github.com/aytugan/ansible-ubuntu-users.git
  name: ubuntu-users
  version: "v1.0.0"
```

Install external module into ~/.ansible/roles folder

```
ansible-galaxy install -r requirements.yml
```

## Usage

playbook.yml:

```
# Configure users
- role: "ubuntu-users"
    vars:
      linux_users:
        - { user: "user1", ssh_key: "ssh-rsa AAAAB3NzaC1yc2E...." }
        - { user: "user2", ssh_key: "ssh-rsa AAAAB3NzaC1yc2E...." }
```        
