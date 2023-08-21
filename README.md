Uma fake API para uma aplicação de scraps

Base URL: https://scrap-fake-api.onrender.com

## ROTAS

## Scraps

### Scraps /scraps GET

Padrão de resposta:

```json
[
   {
      "id": 1,
      "author": "José da Silva",
      "email": "josedasilva@email.com",
      "content": "Belezinha meu amigão?",
      "userId": 1
   }
]
```

### Scraps /scraps POST (Requer Autorização)

```json
{
   "Authorization": "Bearer token"
}
```

Padrão de corpo

```json
{
   "author": "José da Silva",
   "email": "josedasilva@email.com",
   "content": "Belezinha meu amigão?",
   "userId": 1
}
```

Padrão de resposta

```json
{
   "id": 1,
   "author": "José da Silva",
   "email": "josedasilva@email.com",
   "content": "Belezinha meu amigão?",
   "userId": 1
}
```

### Scraps /scraps/:scrapId PATCH (Requer Autorização)

```json
{
   "Authorization": "Bearer token"
}
```

Padrão de corpo

```json
{
   "author": "José da Silva",
   "email": "josedasilva@email.com",
   "content": "Belezinha meu amigão?",
}
```

Padrão de resposta

```json
{
   "id": 1,
   "author": "José da Silva",
   "email": "josedasilva@email.com",
   "content": "Belezinha meu amigão?",
   "userId": 1
}
```

### Scraps /scraps/:scrapId DELETE (Requer Autorização)

```json
{
   "Authorization": "Bearer token"
}
```

Não tem um corpo de resposta, nem precisa de um cor´

## Usuário

## Registrar Usuário /users POST

Padrão de corpo

```json
{
   "name": "José da Silva",
   "email": "josedasilva@email.com",
   "password": "123456"
}
```

## Login de Usuário /login POST

Padrão de corpo

```json
{
   "email": "josedasilva@email.com",
   "password": "123456"
}
```

Padrão de Resposta

```json
{
   "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImpvaG5kb2VAZW1haWwuY29tIiwiaWF0IjoxNjgxMjI2MzU1LCJleHAiOjE2ODEyMjk5NTUsInN1YiI6IjIifQ.HoHzAjg6luV9k6v8zHyewSTHsUnAKDBIbFiIS0r_joM",
   "user": {
      "name": "José da Silva",
      "email": "josedasilva@email.com",
      "id": 1
   }
}
```

### Usuário (Autologin) /users/:userId GET (Requer Autorização)

Headers

```json
{
   "Authorization": "Bearer token"
}
```

Padrão de resposta

```json
{
   "name": "José da Silva",
   "email": "josedasilva@email.com",
   "id": 1
}
```
