<h1 align="center">🚀 Catálogo de Starter Kits</h1>

<p align="center">
  Boilerplates e ambientes de desenvolvimento pré-configurados para acelerar o setup de novos projetos.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJS"/>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white" alt="Prisma"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
</p>

---

## 💡 Sobre este repositório

Este repositório é um "berço" de boilerplates. O objetivo é eliminar as horas gastas configurando infraestrutura, integrando bancos de dados e ajustando ferramentas em cada projeto novo.

Aqui você encontra bases sólidas e arquiteturas padronizadas: é só pegar o kit que atende à sua necessidade e começar direto nas regras de negócio.

## 📚 Kits disponíveis

| Kit | Versão | Stack | Status |
|---|---|---|---|
| [`fullstack-next-nest-postgres`](./fullstack-next-nest-postgres) | v1.0.0 | Next.js · NestJS · PostgreSQL · Prisma · Docker | 🟢 Estável |

## 🛠️ Como usar um kit

Como o repositório tem **vários** kits em subpastas, evite o `git clone` tradicional: ele baixaria todos os kits com o histórico inteiro. Use o [degit](https://github.com/Rich-Harris/degit), que baixa **somente a pasta do template** e entrega um projeto limpo, sem histórico, para você começar o seu versionamento do zero:

```bash
npx degit Vinny1313/starter-kit/NOME_DA_PASTA nome-do-seu-novo-projeto
```

> 💡 Este repositório também é um **Template Repository**. Se preferir, clique em **"Use this template"** no topo da página para gerar uma cópia completa na sua conta.

---

## 🟢 v1.0.0 · `fullstack-next-nest-postgres`

Ambiente de desenvolvimento escalável e focado em produtividade. Todo o ecossistema é conteinerizado, então o famoso *"na minha máquina funciona"* deixa de existir.

### ✨ O que já vem configurado

- 🐳 **Docker zero-config:** o `docker-compose.yml` sobe banco, backend e frontend juntos, comunicando-se por uma rede interna.
- 🧱 **Backend (NestJS):** API modular, com injeção de dependências e TypeScript estrito, na porta `3333` e exposta via `0.0.0.0`.
- 🛡️ **CORS liberado:** `app.enableCors()` configurado no `main.ts`, para o frontend consumir a API sem bloqueios do navegador.
- 🩺 **Health check:** rota `GET /health` que valida, em tempo real, a API e a comunicação com o banco.
- 🗄️ **Banco (PostgreSQL 16):** instância isolada na porta `5432`, com volume persistente.
- 🔗 **Prisma ORM:** `PrismaService` global no NestJS, com consultas tipadas e autocompletar, sem recriar conexões.
- 🖥️ **Frontend (Next.js):** base React na porta `3000`, pronta para consumir o backend.

### 🔌 Portas e serviços

| Serviço | Porta | Descrição |
|---|---|---|
| Frontend | `3000` | Next.js |
| Backend | `3333` | NestJS (`GET /health`) |
| Banco | `5432` | PostgreSQL |

### ▶️ Como rodar

```bash
npx degit Vinny1313/starter-kit/fullstack-next-nest-postgres meu-projeto
cd meu-projeto
docker compose up --build
```

Depois, teste se tudo está de pé:

- Frontend: <http://localhost:3000>
- Health check: <http://localhost:3333/health>

> ⚠️ As credenciais do banco no `docker-compose.yml` são apenas de desenvolvimento. Troque-as e use variáveis de ambiente antes de publicar qualquer coisa em produção.

---

<p align="center">Feito por <a href="https://github.com/Vinny1313">Vinicius Gomes</a></p>
