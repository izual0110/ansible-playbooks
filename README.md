You have to change passwords in hosts 

> sudo ansible-playbook fedora-desktop.yml -i inventories/localhost/hosts

> ansible-playbook create-keys.yml -i inventories/production-unsecure/hosts

> ansible-playbook upload-keys.yml -i inventories/production-unsecure/hosts

> ansible-playbook create-keys-and-upload.yml -i inventories/production-unsecure/hosts

> ansible-playbook fedora-servers.yml -i inventories/production/hosts

> ansible-playbook create-vpn.yml -i inventories/production/hosts

> ansible-playbook create-wireguard.yml -i inventories/production/hosts

> ansible-playbook ubuntu-servers.yml -i inventories/production/hosts

tools work for macos and linux
> ansible-playbook tools.yml -i inventories/production-unsecure/hosts

> ansible-playbook create-wireguard-peer.yml -i inventories/production/hosts

> ssh -i .keys/*_id_rsa 


# Ansible Playbook for SSH Key Generation and Authorization

This Ansible playbook automates the process of creating SSH keys for a list of servers and setting them as authorized keys on the target hosts. Need to fill **inventories/production-unsecure/hosts**
> ansible-playbook create-keys-and-upload.yml -i inventories/production-unsecure/hosts

# Create WG server and peers
> ansible-playbook create-wireguard.yml -i inventories/production/hosts
>
> ansible-playbook create-wireguard-peer.yml -i inventories/production/hosts
>
> qrencode -t ansiutf8 < config
