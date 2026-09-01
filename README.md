# API Connect - Jaqueline Silva

## Descrição
Uma API RESTful simples construída com Node.js e Express para gerenciar usuários. Este projeto é uma atividade acadêmica que demonstra conceitos fundamentais de desenvolvimento de APIs.

## Estrutura do Projeto
```
api-connect-jaqueline-silvajf/
├── src/
│   ├── server.js                 # Arquivo principal do servidor
│   ├── routes/
│   │   └── connectRoutes.js       # Definição das rotas da API
│   ├── controllers/
│   │   └── connectController.js   # Lógica dos controladores
│   └── data/
│       └── mockData.js            # Dados fictícios da API
├── package.json                   # Dependências do projeto
└── README.md                       # Este arquivo
```

## Tecnologias Utilizadas
- **Node.js** - Runtime JavaScript
- **Express.js** - Framework web minimalista
- **Mock Data** - Dados fictícios para testes

## Endpoints da API

### 1. Listar todos os usuários
**GET** `/api/usuarios`

Resposta:
```json
[
  {
    "id": 1,
    "nome": "João Silva",
    "email": "joao@example.com",
    "idade": 28,
    "dataCriacao": "2024-01-15T00:00:00.000Z"
  }
]
```

### 2. Obter um usuário por ID
**GET** `/api/usuarios/:id`

Exemplo: `GET /api/usuarios/1`

Resposta:
```json
{
  "id": 1,
  "nome": "João Silva",
  "email": "joao@example.com",
  "idade": 28,
  "dataCriacao": "2024-01-15T00:00:00.000Z"
}
```

### 3. Criar novo usuário
**POST** `/api/usuarios`

Corpo da Requisição:
```json
{
  "nome": "Novo Usuário",
  "email": "novo@example.com",
  "idade": 26
}
```

Resposta (Status 201):
```json
{
  "id": 5,
  "nome": "Novo Usuário",
  "email": "novo@example.com",
  "idade": 26,
  "dataCriacao": "2024-05-20T10:30:00.000Z"
}
```

### 4. Atualizar um usuário
**PUT** `/api/usuarios/:id`

Exemplo: `PUT /api/usuarios/1`

Corpo da Requisição:
```json
{
  "nome": "João Silva Atualizado",
  "idade": 29
}
```

Resposta:
```json
{
  "id": 1,
  "nome": "João Silva Atualizado",
  "email": "joao@example.com",
  "idade": 29,
  "dataCriacao": "2024-01-15T00:00:00.000Z"
}
```

### 5. Deletar um usuário
**DELETE** `/api/usuarios/:id`

Exemplo: `DELETE /api/usuarios/1`

Resposta:
```json
{
  "mensagem": "Usuário deletado com sucesso",
  "usuario": {
    "id": 1,
    "nome": "João Silva",
    "email": "joao@example.com",
    "idade": 28
  }
}
```

## Como Usar

### Instalação
1. Clone o repositório:
```bash
git clone https://github.com/jaqueline-silvajf/api-connect-jaqueline-silvajf.git
cd api-connect-jaqueline-silvajf
```

2. Instale as dependências:
```bash
npm install
```

### Executar o Servidor
```bash
npm start
```

O servidor será iniciado em `http://localhost:3000`

### Modo Desenvolvimento (com auto-reload)
```bash
npm run dev
```

## Testando a API

Você pode testar a API usando:

### Usando cURL
```bash
# Listar usuários
curl http://localhost:3000/api/usuarios

# Obter usuário específico
curl http://localhost:3000/api/usuarios/1

# Criar novo usuário
curl -X POST http://localhost:3000/api/usuarios \
  -H "Content-Type: application/json" \
  -d '{"nome":"Teste","email":"teste@example.com","idade":25}'

# Atualizar usuário
curl -X PUT http://localhost:3000/api/usuarios/1 \
  -H "Content-Type: application/json" \
  -d '{"nome":"João Atualizado"}'

# Deletar usuário
curl -X DELETE http://localhost:3000/api/usuarios/1
```

### Usando Postman
1. Crie uma nova requisição
2. Selecione o método HTTP (GET, POST, PUT, DELETE)
3. Cole a URL `http://localhost:3000/api/usuarios`
4. Adicione headers se necessário: `Content-Type: application/json`
5. Para POST e PUT, adicione o corpo JSON
6. Clique em Send

## Funcionalidades
✅ Listar todos os usuários  
✅ Buscar usuário por ID  
✅ Criar novo usuário  
✅ Atualizar dados do usuário  
✅ Deletar usuário  
✅ Validação básica de dados  
✅ Tratamento de erros  

## Dados Iniciais (Mock Data)
A API vem com 4 usuários de exemplo pré-carregados:
- João Silva
- Maria Santos
- Carlos Oliveira
- Ana Costa

## Erros Comuns

### Porta já em uso
Se a porta 3000 estiver ocupada, você pode alterar em `src/server.js`:
```javascript
const PORT = 3001; // ou outra porta
```

### Dependências não instaladas
Execute: `npm install`

### Módulos não encontrados
Verifique se o Node.js e npm estão instalados corretamente.

## Licença
MIT

## Autor
Jaqueline Silva

## Data de Criação
Setembro de 2026

---

**Repositório:** [https://github.com/jaqueline-silvajf/api-connect-jaqueline-silvajf](https://github.com/jaqueline-silvajf/api-connect-jaqueline-silvajf)
