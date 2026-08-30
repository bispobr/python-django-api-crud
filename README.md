# API CRUD com Django REST Framework

API REST desenvolvida em Python utilizando Django e Django REST Framework para praticar a implementação das operações CRUD no gerenciamento de usuários.

O projeto também utiliza recursos complementares para integração e acesso à API, incluindo suporte a CORS.

## Funcionalidades

- Listagem de usuários
- Consulta de dados de um usuário por nickname
- Cadastro de usuário
- Atualização de usuário
- Atualização de usuário utilizando nickname na URL
- Exclusão de usuário
- API HTTP baseada em operações CRUD

## Tecnologias

- Python
- Django
- Django REST Framework
- django-cors-headers

## Requisitos

- Python 3+
- Django
- Django REST Framework
- django-cors-headers

## Instalação

Clone o repositório:

```bash
git clone https://github.com/bispobr/python-django-api-crud.git
cd python-django-api-crud
```

Instale as dependências:

```bash
pip install django djangorestframework django-cors-headers
```

## Executando o projeto

Execute o servidor de desenvolvimento Django:

```bash
python manage.py runserver 8080
```

A API estará disponível em:

```text
http://localhost:8080
```

## API Endpoints

### Listar usuários

```http
GET /api/
```

Retorna todos os usuários cadastrados.

### Consultar usuário

```http
GET /api/data/?user={nickname}
```

Retorna os dados do usuário especificado pelo parâmetro `user`.

### Cadastrar usuário

```http
POST /api/data/
Content-Type: application/json
```

Exemplo:

```json
{
  "user_nickname": "usuario",
  "user_name": "Nome do usuário",
  "user_email": "usuario@example.com",
  "user_age": 30
}
```

### Atualizar usuário

```http
PUT /api/data/
Content-Type: application/json
```

O campo `user_nickname` é utilizado para identificar o usuário.

Exemplo:

```json
{
  "user_nickname": "usuario",
  "user_name": "Nome atualizado",
  "user_email": "usuario@example.com",
  "user_age": 31
}
```

### Atualizar usuário pelo nickname

```http
PUT /api/user/{nickname}
Content-Type: application/json
```

Exemplo:

```json
{
  "user_name": "Nome atualizado",
  "user_email": "usuario@example.com",
  "user_age": 31
}
```

### Excluir usuário

```http
DELETE /api/data/
Content-Type: application/json
```

Exemplo:

```json
{
  "user_nickname": "usuario"
}
```

## CORS

O projeto utiliza `django-cors-headers` para fornecer suporte à configuração de Cross-Origin Resource Sharing (CORS).

## Estrutura

O projeto utiliza a estrutura de gerenciamento do Django, tendo `manage.py` como ponto de entrada para os comandos administrativos.

Os detalhes das aplicações, modelos, views e configurações devem ser consultados diretamente na estrutura atual do projeto.

## Comandos úteis

Iniciar o servidor:

```bash
python manage.py runserver 8080
```

Executar migrações:

```bash
python manage.py migrate
```

## Status

Projeto de estudos desenvolvido para praticar a construção de APIs REST CRUD utilizando Python, Django e Django REST Framework.
