#Установка ansible
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
python3 -m pip -V
apt update
apt install ansible
nano /etc/ansible/hosts
###########
[elkservers]
172.16.8.33 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.34 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.35 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.36 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.37 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.7 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.8 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
172.16.8.9 ansible_connection=ssh ansible_user=admin ansible_ssh_private_key_file=~/.ssh/id_rsa ansible_python_interpreter=/usr/bin/python3
############
ssh-keygen -t rsa
ssh-copy-id admin@node
#Запуск плейбука
ansible-playbook site.yml