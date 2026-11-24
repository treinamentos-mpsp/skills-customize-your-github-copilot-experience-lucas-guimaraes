# 📘 Atividade: Criando APIs REST com FastAPI

## 🎯 Objetivo

Construir uma API REST simples em Python usando o framework FastAPI, aprendendo a definir rotas, receber parâmetros, validar dados com modelos Pydantic e implementar operações CRUD.

## 📝 Tarefas

### 🛠️	Primeira Rota

#### Descrição
Instale o FastAPI e crie um arquivo `main.py` com uma aplicação que responda a requisições `GET` na rota raiz `/`.

#### Requisitos
O programa concluído deve:

- Criar uma instância de `FastAPI` chamada `app`.
- Definir uma rota `GET /` que retorne a mensagem `{"message": "Hello, FastAPI!"}`.
- Executar o servidor com `uvicorn main:app --reload` e acessar a rota pelo navegador ou pelo `/docs`.

### 🛠️	Parâmetros de Caminho e de Consulta

#### Descrição
Crie rotas que recebam dados pela URL, tanto no caminho quanto na query string.

#### Requisitos
O programa concluído deve:

- Definir uma rota `GET /greet/{name}` que retorne `{"greeting": "Hello, <name>!"}`.
- Definir uma rota `GET /add` que receba os parâmetros de consulta `a` e `b` (inteiros) e retorne a soma.
- Exemplo de saída para `GET /add?a=3&b=7`:
  ```json
  {"result": 10}
  ```

### 🛠️	Modelos com Pydantic e Requisições POST

#### Descrição
Defina um modelo de dados para um item e crie uma rota que receba esse item no corpo da requisição.

#### Requisitos
O programa concluído deve:

- Criar uma classe `Item` herdando de `BaseModel`, com os campos `name` (texto), `price` (número) e `in_stock` (booleano, com valor padrão `True`).
- Definir uma rota `POST /items` que receba um `Item` e retorne o item recebido acrescido de um campo `id`.
- Retornar erro de validação automático do FastAPI quando o `price` não for um número.

### 🛠️	CRUD de Itens

#### Descrição
Implemente as operações de criar, ler, atualizar e remover itens armazenados em um dicionário em memória.

#### Requisitos
O programa concluído deve:

- Manter os itens em um dicionário em memória, usando o `id` como chave.
- Implementar `GET /items/{item_id}`, `PUT /items/{item_id}` e `DELETE /items/{item_id}`.
- Retornar HTTP 404 com a mensagem `Item not found` quando o item não existir.
- Retornar HTTP 200 para leituras e atualizações e HTTP 204 para remoções bem-sucedidas.
