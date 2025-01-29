# 📌 Aplicação de Movie Notes

Este projeto é uma aplicação desenvolvida em **Node.js** utilizando **SQLite** como banco de dados e **Knex.js** como query builder. A aplicação permite que um usuário cadastrado adicione filmes, fornecendo informações como nome, descrição, nota e tags relacionadas. Além disso, implementa recursos como:

- 🔐 **Criptografia de senhas**;
- 📧 **Validação de e-mail**;
- 🔄 **Cascade delete** para garantir que uma tag será excluída caso a nota correspondente seja removida.

## 🚀 Tecnologias Utilizadas

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)
- [SQLite](https://www.sqlite.org/)
- [Knex.js](https://knexjs.org/)
- [bcrypt.js](https://www.npmjs.com/package/bcryptjs) (para criptografia de senhas)

---

## 📂 Estrutura do Projeto

```bash
📦 projeto
├── 📁 src
│   ├── 📁 database
│   │   ├── 📁 sqlite
│   │   │   ├── 📁 migrations  # Diretório para migrações do banco SQLite
│   │   │   └── database.db  # Arquivo do banco de dados gerado
│   │   ├── 📁 knex
│   │   │   ├── 📁 migrations  # Diretório para migrações do Knex
│   │   │   └── knexfile.js  # Configuração do Knex
│   ├── 📁 routes
│   ├── 📁 controllers
│   ├── server.js
├── package.json
└── README.md
```

---

## 📌 Configuração e Uso

### 1️⃣ Clonar o Repositório
```bash
git clone https://github.com/ncandreassa/rs-nodejs-11.git
cd seu-repositorio
```

### 2️⃣ Instalar Dependências
```bash
npm install
```

### 3️⃣ Executar a Aplicação
Inicie o servidor em ambiente de desenvolvimento com:
```bash
npm run start dev
```
Isso criará automaticamente o arquivo **database.db** na pasta `src/database/sqlite/`.

### 4️⃣ Criar as Tabelas no Banco de Dados
Rodar as migrações para criar as tabelas necessárias:
```bash
npm run migrate
```

### 5️⃣ Testar a API
Para testar as funcionalidades da API, você pode utilizar o **Insomnia** ou outro cliente HTTP, como **Postman**. Basta configurar as requisições para interagir com as rotas disponíveis.

---

## 🎯 Endpoints Principais

### 🔹 Usuários
- **`POST /users`** - Criar um novo usuário.
- **`PUT /users/:id`** - Atualizar um usuário.

### 🔹 Filmes
- **`POST /notes`** - Criar uma nova nota de filme.
- **`GET /notes/:id`** - Listar uma nota.
- **`GET /notes`** - Listar todas as notas.
- **`DELETE /notes/:id`** - Excluir uma nota (tags associadas são removidas automaticamente).

### 🔹 Tags
- **`GET /tags`** - Listar todas as tags de filmes.

---

## 🛠️ Ferramentas Recomendadas

- [Beekeeper Studio](https://www.beekeeperstudio.io/) - Para visualizar e gerenciar o banco SQLite.
- [Insomnia](https://insomnia.rest/) - Para testar os endpoints da API.

---

