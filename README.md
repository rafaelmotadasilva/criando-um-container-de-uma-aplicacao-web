<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> Criando um Container de uma Aplicação WEB</span>
</h1>

Repositório desenvolvido para fins educativos.

## Objetivo
Executar uma aplicação HTML em um Container Apache utilizando o Docker Compose.

## O Docker Compose

Este é um exemplo simples de Docker Compose, no entanto, há muitas opções que podem ser incluídas nesse arquivo de YAML.

```
version: '3.9'
volumes:
  htdocs:
services:
  app:
    image: httpd:latest
    container_name: my-apache-app
    restart: always
    ports:
    - '80:80'
    volumes:
    - htdocs:/usr/local/apache2/htdocs
```
Em seguida, em um terminal, execute o seguinte comando:

```
sudo docker-compose up -d
```