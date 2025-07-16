# Installation of Ansible
- Add reposiotory
```bash
sudo apt-add- repository ppa:ansible/ansible
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
