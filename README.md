# python-django-api-crud

Este repositório contém um projeto CRUD simples construído usando django. O objetivo deste repositório é praticar e construir todos os métodos CRUD usando python.

## Instalação

1. Clone o repositório:

```bash
git https://github.com/bispobr/python-django-api-crud.git
```
2. instale o django, djangorestframework, django-cors-headers através do pip python
2. execute o arquivo manage.py

## Como usar

1. API está acessivel através do Link http://localhost:8080

## API Endpoints
API contem os seguintes endpoints :

```http request
GET api/ - Retorna todos os usuários.

GET api/data/?user=usuario - Retorna dados do usuário especificado.
```

```http request
POST api/data/ - cadastra um novo usuário.
Content-Type: application/json

{
    "user_nickname": "xxx",
    "user_name": "xxxxx",
    "user_email": "xxx.xxxxx@xxx.xxx",
    "user_age": 000
}
```
```http request
PUT api/data/ - Altera  informações de um usuário.

Content-Type: application/json - obs: o parametro user_nickname é obrigatorio

{
    "user_nickname": "xxx",
    "user_name": "xxxxx",
    "user_email": "xxx.xxxxx@xxx.xxx",
    "user_age": 000
}

```
PUT forma 2 - passagem de nickname atraves da url

```http request
PUT api/user/usuario - Altera  informações do usuário.

Content-Type: application/json 

{
    "user_name": "xxxxx",
    "user_email": "xxx.xxxxx@xxx.xxx",
    "user_age": 000
}
```

```http request
DELETE api/data/ - Exclui usuário.

Content-Type: application/json

{
   "user_nickname": "xxx",
}
```