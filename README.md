# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada,

## Endpoints

A api tem um total de 5 endpoints, e tem o objetivo de criar uma lista de produtos para a Hamburgeria e adicionar itens ao carrinho

### Cadastro

POST /register

### Login

POST /login

## Products

Neste endpoint é possivel visualizar todos os produtos disponiveis.

`GET- /products`

Authorization: ` Bearer Token`

`FORMATO DA RESPOSTA - STATUS 201`

```json
[
  {
    "name": "Hamburger",
    "category": "Sanduiche",
    "image": "https://www.pngall.com/wp-content/uploads/5/Hamburger-PNG-Free-Image.png",
    "price": "14,00"
  },
  {
    "name": "X-Burguer",
    "category": "Sanduiche",
    "image": "https://www.pngall.com/wp-content/uploads/5/Fast-Food-Tofu-Burger-PNG-Free-Download.png",
    "price": "16,00"
  }
]
```

Token necessário :

`FORMATO DA RESPOSTA - STATUS 401`

```json
"Missing token"
```

`GET- /cart?userId=1`

Authorization: ` Bearer Token`

`FORMATO DA RESPOSTA - STATUS 201`

```
json
[
  {
    "name": "Hamburger",
    "category": "Sanduiche",
    "image": "https://www.pngall.com/wp-content/uploads/5/Hamburger-PNG-Free-Image.png",
    "price": "14,00",
    "userId": 1,
    "id": 1

  }
]
```
