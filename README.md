# Install Various Dev Environments on Ubuntu

Windows WSL env
Ansible 2.9
Target environment is my home environment
pre-req:
- install hyper-v ubuntu vm via quick create - should automate this at some point
- 
- install ssh-server on vm `sudo apt install ssh-server -y`
- update /etc/netplan/{network.yml}
  - `ls /etc/netplan`
  - `cp /etc/netplan/01-network-manager-all.yaml /etc/netplan/01-network-manager-all.yaml.bk`
  - `sudo nano /etc/netplan/01-network-manager-all.yaml`
```

```
- run `ssh-copy-id <username>@vm_ip`
- verify ssh works with no password

## Network setup


## TODOs

- move all of this to docker

## Running Playbook

- `ansible-playbook deploy_flask_env/flask_env_setup.yml -i development_servers/hosts --extra-vars ansible_sudo_pass='<password>'`

