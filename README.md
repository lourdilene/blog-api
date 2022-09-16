# Blog-api

Está aplicação utiliza o Docker containers, eis a lista:

* mysql - Database server
* laravel - API

## Como utilizar

### 1. Preparação

Clone o repositório do github e mude de diretório de trabalho

    git clone https://github.com/lourdilene/blog-api.git
    cd blog-api    

Dentro de `docker-compose.yml` você precisa alterar os valores para o que você precisa.

Execute o seguinte comandando para criar os containers

    sail up

### 2. Instale todas as dependências necessárias

Acesse o container laravel:

    docker-compose exec -it blog-api-laravel.test-1 bash

Instale todas as dependências

    composer install

### 3. Configuração da aplicação

Crie as databases

    php artisan migrate

### 4. EndPoint Post

Método Store
http://localhost/api/post

    {
        "title": "Titulo do Post",
        "body": "Conteúdo do Post"
    }

## Fim

Obrigada :)
