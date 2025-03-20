# Ansible playbook for setting up my raspberry pi

used on
- raspberry pi4
  -  ubuntu 24.04

- Ansible controller:
  - Ubuntu 24.04 on wsl
  - ansible [core 2.17.9], python version = 3.12.3


notes along the way

---
Because i use ssh key

ssh-agent bash
ssh-add ~/.ssh/id_rsa

Check the connection with your raspi
ansible -m ping -i inventory/all pi4

ansible-playbook site.yml -i inventory/all 

lil note 
(\.|^)s\.youtube\.com$


