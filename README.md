<h1 align="center">Atividade 5A04 - JSON-SERVER - by Anderson Silva</h1>

url da api https://server-anderson-motorbikes.herokuapp.com/

## Rotas que não necessitam de autenticação

<h3 align='center'> Cadastro de usuário</h3>

`POST /register - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "kenzinho@mail.com",
  "password": "$2a$10$YQiiz0ANVwIgpOjYXPxc0O9H2XeX3m8OoY1xk7OGgxTnOJnsZU7FO",
  "name": "Kenzinho",
  "age": 38
}
```

<h3 align='center'> Login </h3>

`POST /login - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "kenzinho@mail.com",
  "password": "123456"
}
```

<h3 align='center'> Lista Motocicletas </h3>

`GET /motorcycles - FORMATO DA RESPOSTA - STATUS 200`

```json
{
      "brand": "Suzuki",
      "model": "GSX",
      "year": 2014,
      "userId": 2,
      "id": 1
    },
    {
      "brand": "Honda",
      "model": "Bis",
      "year": 2014,
      "userId": 1,
      "id": 2
    },
```

## Rotas que necessitam de autenticação


Necessita autorização de token

> Authorization: Bearer {token}

Após logado ele deve conseguir criar/ver as mecânicas cadastradas

<h3 align='center'> Criar mecânicas </h3>

`POST /machineShops - FORMATO DA RESPOSTA`


```json
{
	"name": "Reparos 2 rodas",
      "address": {
        "state": "SC",
        "city": "Camboriú",
        "district": "Rio Pequeno",
        "street": "Rio das Flores",
        "number": 438
      }
}
```

<h3 align='center'> Ver mecânicas </h3>

`GET /machineShops - FORMATO DA RESPOSTA - STATUS 200`

```json
{
    "name": "Reparos 2 rodas",
    "address": {
      "state": "SC",
      "city": "Camboriú",
      "district": "Rio Pequeno",
      "street": "Rio das Flores",
      "number": 438
    },
    "id": 1
  }
```
Após logado ele deve conseguir criar as motos cadastradas

<h3 align='center'> Criar motos </h3>


```json
{
      "brand": "Suzuki",
      "model": "GSX-R",
      "year": 2020,
      "userId": 2
}
```