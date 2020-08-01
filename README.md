# test_Ubuntu_wsl
Ansible on Ubuntu on Windows (WSL)

This is my first post on github... 
OK this time I will try to install ansible on Ubuntu (This should be a piece of cake)

# Environment: 
Windows 10 Home edition Ver. 1909
WSL version: 4.4.0-18362 (Version 1)
Ubuntu 20.04 LTS
Guest VM: Linux Mint 20 on VirtualBox 


# Notes to self:
- Always start with ansible -m ping, before rushing with with playbook
```
ansible -i inventory/all linuxes -m ping
```
- Linux Mint doesn't come with openssh-server. You have to install it
- On the ansible host, install sshpass to be able to enter user password. Ansible will prompt you anyway if there is no sshpass
- '-' Hyphen seems not to be a good idea for names
- OMG OMG you can disable host key checking in ansible.cfg: host_key_checking = False


## generate roles structure
With ansible-galaxy command

move to the folder
```
cd roles/
```
run this galaxy command
```
ansible-galaxy init common
```
# ref: 
Installation official ansible website
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-ubuntu

setup my ansible folder
https://www.howtoforge.com/ansible-guide-create-ansible-playbook-for-lemp-stack/