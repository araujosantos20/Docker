## Criar um contêiner em Docker

~~~Docker
`docker run --name mateus –p 6556:3306 –v dados:/var/lib/mysql –e MYSQL_ROOT_PASSWORD=mateus123 –d mysql`
~~~

Explicação de cada item para a criação de um contêiner em Docker:

- `--name` é aonde você nomeará seu contêiner na hora da criação

- `-p` é a porta de comunicação que você utilizará para poder utilizar seu contêiner com outras ferramentas.

- `-v` é o volume, ou a pasta que será armazenada as informações e memória do Docker.

- `-e` é a senha do seu Docker que você irá definir.
Utilizei também MYSQL_ROOT_PASSWORD= para definir a senha no MySQL

- `-d` é a imagem que você utilizará do software, especificando a versão ou apenas colocando o nome, assim fazendo o Docker entender que será a versão mais atual.

### Comandos básicos do Docker

Para ter mais informações do Docker assim que criado, utilize:

~~~Go
docker ps -a
~~~

Assim você terá mais informações do seu Docker como:

ID | Nome_Docker | Porta de Comunicação

Além de ver quantos docker você tem e as informações de cada um deles.
---

Para ativar seu Docker, apenas insira o comando:

~~~
docker start mateus
~~~

E depois disso já está ativado seu Docker, mas se quiser confirmar o Status do Docker, você pode usar o comando 
~~~
Docker ps -a
~~~

E você conseguirá visualizar se o Docker já está ativo ou não.

---

Para parar de rodar o Docker, utilize
~~~
Docker stop
~~~
E assim o Docker será desligado.

---
E para excluir um Docker utilize o comando 
~~~
docker rm ma
~~~
após o RM utilize os últimos 2 caracteres do ID do contêiner que você queira excluir.