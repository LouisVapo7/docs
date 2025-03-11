# Vapo Bytes CPF - Documentação da API

Bem-vindo à documentação da API de Consulta de CPF da **Vapo Bytes**. Esta API foi projetada para fornecer uma forma fácil e segura de consultar informações de CPF.

## Sumário

- [Introdução](#introdução)
- [Referência da API](#referencia-da-api)
- [Início Rápido](#inicio-rapido)
- [Autenticação](#autenticacao)
- [Exemplo de Uso](#exemplo-de-uso)

---

## Introdução

A API de Consulta de CPF da **Vapo Bytes** é uma ferramenta poderosa para consultar informações de CPF de forma rápida e segura. Com esta API, você pode consultar informações de CPF de forma fácil e eficiente.

---

## Referência da API

### **Consulta de CPF**

**Requisição:**
```http
GET /consulta/{token}/{cpf}
```

**Parâmetros:**

| Parâmetro | Tipo   | Descrição                     |
|------------|--------|--------------------------------|
| `token`   | string | Token de acesso da API.       |
| `cpf`     | string | Número do CPF a ser consultado. |

**Resposta:**

```json
{
  "status": 200,
  "requests": 10,
  "dados": {
    "nome": "João da Silva",
    "sexo": "Masculino",
    "data_nascimento": "01/01/1990"
  }
}
```

| Campo            | Tipo   | Descrição                                 |
|-----------------|--------|-----------------------------------------|
| `status`       | int    | Código de status da resposta (200, 404, etc.). |
| `requests`     | int    | Número de requisições realizadas com o token. |
| `dados`        | objeto | Informações do CPF consultado.                |
| `nome`         | string | Nome completo do titular do CPF.         |
| `sexo`         | string | Sexo do titular do CPF.                  |
| `data_nascimento` | string | Data de nascimento do titular do CPF.    |

---

## Início Rápido

Para começar a usar a API, siga os passos abaixo:

1. Obtenha um **token de acesso**.
2. Realize uma requisição **GET** para o endpoint de consulta de CPF.
3. Insira o **token de acesso** e o **CPF** que deseja consultar.
4. Receba a resposta com as informações do CPF consultado.

---

## Autenticação

Para acessar a API, é necessário utilizar um **token de acesso**. Você pode obter um token ao se registrar em nossa plataforma.

**Exemplo de uso do token na requisição:**
```http
GET /consulta/SEU_TOKEN/12345678900
```

---

## Exemplo de Uso

Aqui está um exemplo de como consumir a API usando **cURL**:

```sh
curl -X GET "https://api.vapobytes.com/consulta/SEU_TOKEN/12345678900"
```

Ou utilizando **Python (requests)**:

```python
import requests

token = "SEU_TOKEN"
cpf = "12345678900"
url = f"https://api.vapobytes.com/consulta/{token}/{cpf}"

response = requests.get(url)
print(response.json())
```

---

Feito com ❤️ pela equipe **Vapo Bytes**.
