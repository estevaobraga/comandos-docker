# Comandos Docker
Copilado de comandos para manipulação de containers docker

#### Hello docker
Testando o ambiente, um exemplo mínimo.
```
docker run hello-world
```

#### Baixar uma imagem
Pesquise imagens em: https://hub.docker.com/
```
docker pull nome_imagem
```

#### Criar um container
**Criar um container**
```
docker run -p porta_ip_host:porta_ip_container --name nome -d imagem
```
**Rodar MySQL em um container**
```
docker run --name BaseMySQL -e MYSQL_ROOT_PASSWORD=senha -p 3306:3306 -d mysql
```
_-d: roda em backgroud_
_-p: configuração de exposição da porta ip_
_-e: configurações de variável_
_-t: modo interativo_
#### Manipulando containers
**Listar Containers rodando**
```
docker ps
```
**Listar containers parados**
```
docker ps -f "status=exited"
```
**Parar um container**
```
docker stop nome ou id_container
```
**Excluir um container**
```
docker rm nome ou id_container
```
**Excluir todos os containers**
```
docker rm -f $(docker ps -aq)
```
**Acessar terminal do container**
```
docker exec -it nome_container bash
```
#### Manipular imagens docker
**Salvar imagem, criar arquivo**
```
docker save -o imagem.docker imagem
```
**Carregar imagem**
```
docker load -i umagem.docker
```
**Buildar/Criar uma imagem apartir de um dockerfile**
```
docker build -t nome_imagem .
```
