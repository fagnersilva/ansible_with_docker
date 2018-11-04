# Executando Tasks

### Executando o módulo ping para testar a comunicação com os hosts: 
```ansible
ansible -m ping all
```

### Executando comandos
```ansible
ansible -m command -a "hostname" all`
```
ou  

```ansible
ansible -a "hostname" all
```

[Documentação dos Módulos](https://docs.ansible.com/ansible/latest/modules/list_of_all_modules.html)
