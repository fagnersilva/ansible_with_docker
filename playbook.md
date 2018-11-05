# Criando o nosso primeiro Playbook

### O que é um Playbook?

_Playbooks são a forma pelo qual o Ansible consegue configurar uma política ou passos de um processo de configuração. São feitos para serem fáceis de ler e podem realizar desde deploys de máquinas remotas até delegar ações com diferentes hosts através da interação com servers de monitoramento._

### Crie um diretorio "playbooks"
> `mkdir /etc/ansible/playbooks`

### Criando nosso primeiro arquivo para receber os commandos

>`touch /etc/ansible/playbooks/hostname.yml`

### Adicionando 
>`sudo vim /etc/ansible/playbooks/hostname.yml`

### Exemplo de playbook
[hostname.yml](https://github.com/fagnersilva/ansible_with_docker/blob/master/playbooks/hostname.yml)

### Executando o playbook
> `ansible-playbook /etc/ansible/playbooks/hostname.yml`

## Módulo APT
[nginx.yml](https://github.com/fagnersilva/ansible_with_docker/blob/master/playbooks/nginx.yml)

## Módulo APT instalando Banco de dados
[db.yml](https://github.com/fagnersilva/ansible_with_docker/blob/master/playbooks/db.yml)
