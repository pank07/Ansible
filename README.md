# Installation of Ansible
- Add reposiotory
```bash
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
  ```
- Install ansible
```bash
sudo apt install ansible
```
```bash
sudo vim /etc/ansible/hosts
ansible-inventory --list -y
```
```bash
[servers]
server1 ansible_host=<Public_IP>
server2 ansible_host=<Public_IP>
server3 ansible_host=<Public_IP>

[all:vars]
anisble_python_interpreter=/usr/bin/python3
ansible_user=ubuntu
ansible_ssh_private_key_file=/<file>
```
-Ansible Adhoc commands vs modules
ad hoc commands are great for tasks you repeat rarely.
-a is used for adhoc commands ansible all -a "df -h" -u ubuntu ansible servers -a "uptime" -ubuntu
```bash
ansible servers -a "free -h"
```
-Ansible modules are units of code that can control system resource or execute system commands
-eg. -m is used for modules ansible all -m ping -u ubuntu
```bash
ansible servers -m ping
```
