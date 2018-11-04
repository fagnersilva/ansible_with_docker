# Executando Tasks

### Executando o módulo ping para testar a comunicação com os hosts: 
>`ansible -m ping all`

### Executando comandos
>`ansible -m command -a "hostname" all`

ou  

>`ansible -a "hostname" all`


[Todos os Módulos](https://docs.ansible.com/ansible/latest/modules/list_of_all_modules.html)
