## Listando os hosts:

### Lista todos os hosts:
>`ansible --list-hosts all`   
ou   
>`ansible --list-hosts "*"`

### Lista hosts por grupo
>`ansible --list-hosts containers`

### Lista hosts por IP
>`ansible --list-hosts 172.17.0.2`

### Lista todos hosts da faixa de IP
>`ansible --list-hosts 172.17.0.*`

### Lista os hosts de dois grupos
>`ansible --list-hosts Control:containers`

### Lista os hosts menos do grupo:
>`ansible --list-hosts \!containers`

### Lista os hosts por posição:
>`ansible --list-hosts [0]`
