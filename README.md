# 💰 Financial Tracker API

API REST desenvolvida com **NestJS** para gestão financeira pessoal, permitindo autenticação segura baseada em cookies HTTP-only e gerenciamento de transações com controle de acesso por roles.

---

## 📌 Objetivo

Construir uma API backend estruturada, segura e escalável, aplicando boas práticas de arquitetura modular, validação de dados e controle de autorização.

---

## 🚀 Tecnologias Utilizadas

- NestJS
- Node.js
- MongoDB
- JWT
- HTTP-only Cookies
- Guards (RBAC)
- Class-validator
- Swagger (OpenAPI)
- CORS

---

## 🔐 Autenticação e Segurança

- Login com JWT assinado
- Token armazenado em cookie HTTP-only
- Proteção de rotas com Guards
- Controle de acesso por roles
- Validação de entrada com DTOs
- CORS configurado por variável de ambiente
- Isolamento de dados por usuário autenticado

---

## 📂 Estrutura do Projeto

<pre>
app/
└── src/
    └── modules/
        ├── auth/
        ├── users/
        │   ├── dto/
        │   ├── entities/
        │   ├── users.controller.ts
        │   ├── users.service.ts
        │   └── users.module.ts
        │
        └── transactions/
            ├── dto/
            ├── entities/
            ├── transaction.controller.ts
            ├── transaction.service.ts
            └── transaction.module.ts
</pre>

### Organização aplicada:

- **Controllers** → Responsáveis por receber requisições HTTP
- **Services** → Contêm a regra de negócio
- **DTOs** → Validação e tipagem dos dados de entrada
- **Entities** → Representação das estruturas persistidas no banco
- **Modules** → Separação por domínio
- **Guards** → Autorização e proteção de rotas

---

## 📊 Funcionalidades

- Registro de usuários
- Login com autenticação JWT
- Autorização baseada em roles
- CRUD de transações financeiras
- Associação de transações ao usuário autenticado
- Documentação interativa com Swagger

---

## 📄 Documentação da API

Após iniciar o servidor, a documentação estará disponível em: localhost:3000/api

## ⚙️ Configuração do Ambiente

1️⃣ Clone o repositório:

- git clone https://github.com/DiegoFiuza/Financial-tracker.git
- cd Financial-tracker

2️⃣ Instale as dependências npm install

3️⃣ Configure as variáveis de ambiente Crie um arquivo .env na raiz do projeto com base no .env.
example: MONGODB_URI=SEU_DATABASE
SECRET=SECRET_DE_JWT
ORIGIN=URL_DE_ORIGEM_PERMITIDA
Descrição das variáveis MONGODB_URI → String de conexão com o MongoDB
SECRET → Chave usada para assinatura do JWT
ORIGIN → URL autorizada para requisições (CORS)
⚠️ O arquivo .env não deve ser versionado.

4️⃣ Execute o projeto npm run start:dev

## 🧠 Conceitos Aplicados

- Arquitetura modular escalável
- Separação de responsabilidades
- Autenticação baseada em token
- Autorização por roles
- Validação de dados com DTO
- Estrutura preparada para evolução e expansão

## 👨‍💻 Autor

- Diego Fiuza
- Backend Developer focado em Node.js e NestJS
