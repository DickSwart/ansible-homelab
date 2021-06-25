# Automation with Ansible

## install

```bash
sudo apt update
sudo apt install ansible
sudo apt install sshpass
```

`hosts`

```ini
[ubuntu]
server-01
server-02
192.168.0.100
192.168.0.1002
```

## commands

command with module

```bash
ansible -i ./inventory/hosts ubuntu -m ping --user someuser --ask-pass
```

command with playbook


```bash
ansible-playbook ./playbooks/apt.yml --user someuser --ask-pass --ask-become-pass -i ./inventory/hosts
```

## Referance
- [Ansible documentation](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
- [Ansible Vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html)
- [Techno Tim - Automate EVERYTHING with Ansible! Video](https://www.youtube.com/watch?v=w9eCU4bGgjQ)