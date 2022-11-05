1. 
problem:
ошибка устанновки коллеции ансибла, из-за старой версии (нужна версия ансибл выше 2.9)

root@autolab72:~/diplom/ansible/roles# ansible-galaxy collection install nginxinc.nginx_core
- downloading role 'collection', owned by
 [WARNING]: - collection was NOT installed successfully: ERROR! Content has no field named 'owner'

ERROR! - you can use --ignore-errors to skip failed roles and finish processing the list.

how to fix:
0)
Установка python3.10
https://cloudbytes.dev/snippets/upgrade-python-to-latest-version-on-ubuntu-linux
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
apt install python3.10


a)
apt install python3-pip

b)
Сделать по умалчанию python3 вместо pthon2.7
update-alternatives --install /usr/bin/python python /usr/bin/python3.10 10  ##Обязательно указать приоритет


c)
Обновляем ансибл
pip install ansible




