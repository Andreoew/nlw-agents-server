# NLW Agentes - Server

Backend do projeto **NLW Agentes** desenvolvido durante o evento NLW (Next Level Week) da Rocketseat.

## 🚀 Tecnologias

- **Node.js** - Runtime JavaScript
- **TypeScript** - Linguagem de programação
- **Fastify** - Framework web rápido
- **Drizzle ORM** - ORM para PostgreSQL
- **PostgreSQL** - Banco de dados relacional
- **Zod** - Validação de schemas
- **Docker** - Containerização

## 📋 Pré-requisitos

- Node.js 18+
- Docker e Docker Compose
- PostgreSQL (via Docker)

## 🛠️ Configuração

1. **Clone o repositório**
```bash
git clone <url-do-repositorio>
cd server
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure as variáveis de ambiente**
Crie um arquivo `.env` na raiz do projeto:
```env
PORT=3333
DATABASE_URL=postgresql://docker:docker@localhost:55432/agents
```

4. **Inicie o banco de dados**
```bash
docker-compose up -d
```

5. **Rode as migrações**
```bash
npx drizzle-kit migrate
```

6. **Execute o seed do banco de dados**
```bash
npm run db:seed
```

7. **Inicie o servidor**
```bash
# Desenvolvimento
npm run dev

# Produção
npm start
```

## 📁 Estrutura do Projeto

```
src/
├── db/
│   ├── connection.ts    # Conexão com banco
│   ├── schema/          # Schemas do Drizzle
│   └── migrations/      # Migrações do banco
├── http/
│   └── routes/          # Rotas da API
├── env.ts              # Configuração de variáveis
└── server.ts           # Servidor principal
```

## 🔧 Scripts Disponíveis

- `npm run dev` - Inicia o servidor em modo desenvolvimento
- `npm start` - Inicia o servidor em modo produção
- `npm run db:seed` - Executa o seed do banco de dados

## 🌐 Endpoints

- `GET /health` - Health check da aplicação
- `GET /rooms` - Lista as salas disponíveis

## 📝 Padrões de Projeto

- **Clean Architecture** - Separação de responsabilidades
- **Type Safety** - TypeScript com validação Zod
- **Database First** - Drizzle ORM com PostgreSQL
- **RESTful API** - Endpoints REST
- **Environment Variables** - Configuração via variáveis de ambiente

---

Desenvolvido com 💜 durante o NLW da Rocketseat 