# Utilizando Ansible com Docker
[![License][license-badge]][license-url] [![License][PyPI-version]][license-ansible]

## **O que é Ansible?**
> É uma ferramenta de gerenciamento e provisionamento de configurações.

### Instalar o Ansible no Ubuntu.

>`sudo easy_install pip`
>`sudo pip instalar ansible`

### Agora o Ansible está instalado.

>`ansible --version`

## O que é Docker?

### fazeendo download da image ubuntu 16.04
> `docker pull ubuntu:16.04`

### Iniciando um container Ubuntu
> `docker run -t -d --name ubuntu ubuntu:16.04`

### Conectando no container Ubutu
> `docker exec -it ubuntu /bin/bash`

### Instalando alguns pacotes
> `apt-get update && apt-get upgrade -y && apt-get install openssh-server openssh-client vim build-essential sudo python -y`

### Iniciando o SSH
> `/etc/init.d/ssh start`


----
## Crie um usuário diferente de root:

> `adduser fsantoss | password 123456`

> `adduser fsantoss sudo`

> `visudo`  
> `%sudo   ALL=(ALL) NOPASSWD: ALL`


> `mkdir /home/fsantoss/.ssh`

### No desktop rodar o comando abaixo
> `cat ~/.ssh/id_rsa.pub | sua chave publica do seu notebook`

Em seguida, copie a chave pública para:

> `vim /home/fsantoss/.ssh/authorized_keys`

### Acessando via SSH o Container

> `docker ps -q`

> `docker inspect "id_container" --format '{{.NetworkSettings.IPAddress}}'`

> `docker exec -it "id_container" bash -c "/etc/init.d/ssh status"`

> `docker exec -it "id_container" bash -c "/etc/init.d/ssh restart"`

### Criando um grupo no hosts do Ansible
> `vim /etc/ansible/hosts`

> `[containers]`  
> `172.17.0.3`
### Testando comunicação com o host cadastrado
> `ansible containers -m ping`

### Instalando o nginx no Container
> `ansible containers -s -m apt -a 'pkg=nginx state=installed update_cache=true'`

### Iniciando o Nginx
> `docker ps -q`
> `docker exec -it "id_container" bash -c "/etc/init.d/nginx start"`

[license-badge]: https://img.shields.io/github/license/robertoachar/generator-oss-project.svg
[license-url]: https://opensource.org/licenses/MIT

[PyPI-version]: https://img.shields.io/pypi/v/ansible.svg
[license-ansible]:  https://pypi.org/project/ansible
