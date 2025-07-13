# 🧠 NLWAGENTS

Este projeto foi desenvolvido em colaboração durante o evento **NLW Agentes**, promovido pela [Rocketseat](https://rocketseat.com.br). Seu objetivo é consolidar conhecimentos em back-end com TypeScript, banco de dados relacional, e orquestração de ambientes com Docker.

> ⚠️ Embora o projeto tenha sido iniciado durante o evento, foram feitas melhorias adicionais como organização avançada das pastas, uso do Drizzle ORM e configuração com Docker Compose.

---

## 📦 Estrutura de Pastas


```
├── docker
│ └── setup.sql # Script inicial do banco
├── node_modules # Dependências do projeto
├── src
│ ├── db
│ │ ├── migrations
│ │ │ ├── meta
│ │ │ │ ├── _journal.json
│ │ │ │ ├── 0000_snapshot.json
│ │ │ └── 0000_first_ink.sql
│ │ └── schema
│ │ ├── index.ts
│ │ ├── rooms.ts
│ │ └── connection.ts
│ ├── env.ts
│ └── server.ts
├── .env # Variáveis de ambiente
├── biome.jsonc # Configuração do Biome
├── docker-compose.yml # Orquestração dos containers
├── drizzle.config.ts # Configuração do Drizzle ORM
├── LICENSE
├── package.json
├── package-lock.json
├── tsconfig.json # Configuração do TypeScript
└── README.md
```

---

## 🚀 Tecnologias Utilizadas

- **Node.js** com **TypeScript**
- **Drizzle ORM** (migrations e schemas tipados)
- **SQLite** ou outro banco relacional (via Docker)
- **Docker e Docker Compose**
- **dotenv** para variáveis de ambiente
- **Biome** para formatação e lint
- **Vite / tsx / zod** (opcional, se usado no projeto)

---

## ⚙️ Como rodar o projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/NLWAGENTS.git
cd NLWAGENTS


2. Instale as dependências

npm install

---

3. Configure o .env

Crie um arquivo .env na raiz do projeto com base no .env.example (se houver), ou configure as variáveis necessárias para o banco de dados.

---

4. Suba os containers com Docker

docker-compose up -d

Obs: Isso irá subir o banco de dados e aplicar o script setup.sql automaticamente.

---

5. Rode o servidor de desenvolvimento

npm run dev

---

🗃️ Banco de Dados & Migrations

As migrations estão localizadas em:

src/db/migrations/

Obs: Elas são gerenciadas pelo Drizzle ORM e acompanham arquivos de meta (_journal.json, snapshot) e o SQL gerado (0000_first_ink.sql).

```
---

### 🛠️ Scripts Disponíveis

* npm run dev — Inicia o servidor com hot-reload

* npm run build — Compila o projeto

* npm run lint — Roda o linter com o Biome

* docker-compose up — Sobe os serviços (DB)

* docker-compose down — Para os containers

---  

### 📌 Considerações

* Projeto focado em boas práticas modernas, com separação entre schema,   migrations e server.

* Uso de tipagens seguras com TypeScript e ORM baseado em types com Drizzle.

* Estrutura pensada para escalar facilmente e integrar com front-end futuramente.

---

## ⚙️ licença


Esse projeto está sob a licença [MIT](./LICENSE).  
<a href="./LICENSE">
  <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-brightgreen.svg" />
</a>

---

### 👨‍💻 Autor

* Desenvolvido por Gabriel Moura durante o NLW Agentes 🚀
Focado em transformar ideias em aplicações modernas, performáticas e organizadas.