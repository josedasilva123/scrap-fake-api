Uma fake API para uma aplicação de scraps

Base URL: https://scrap-fake-api.onrender.com

## ROTAS

### Scraps /scraps GET

Padrão de resposta:

```json
[
    {
        "id": 1,
        "author": "José da Silva",
        "email": "josedasilva@email.com",
        "content": "Belezinha meu amigão?",
    } 
]
```

### Scraps /news POST

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
} 
```