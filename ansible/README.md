# Ansible

## Installation

<https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html>

## Add Hosts

```bash
sudo nano /etc/ansible/hosts
```

```
[GROUP]
<<host name>> ansible_host=<<ip address>> ansible_connection=ssh ansible_ssh_user=<<user>> ansible_ssh_pass=<<password>>
```

## Command to run playbook

```
ansible-playbook <<file>> -K
```
