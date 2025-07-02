# 🧪 Projeto Node.js API REST com Hapi.js e PostgreSQL

> Projeto acadêmico desenvolvido por **Cláudio Matos** e **Felipe Ferreira**, estudantes de Desenvolvimento de Software Multiplataforma (DSM) na **Fatec Franca**.  
> Esta API foi construída com **Node.js**, usando o **framework Hapi.js**, validação com **Joi**, e persistência de dados com **Sequelize** + **PostgreSQL**.

---

## 🚀 Visão Geral

Esta aplicação oferece uma **estrutura base para criação de APIs RESTful**, com funcionalidades de **CRUD para gerenciamento de produtos e alunos**.

O projeto foi iniciado na disciplina de **Laboratório Web** e serve como um modelo funcional e didático para projetos com foco em back-end.

---

## 🧰 Tecnologias e Bibliotecas

- 🔷 **Node.js** — ambiente de execução JavaScript
- 🌐 **@hapi/hapi** — framework web e de APIs
- ✅ **Joi** — biblioteca para validação de dados
- 🧬 **Sequelize** — ORM para banco relacional
- 🐘 **PostgreSQL** — banco de dados relacional
- 🔌 **pg** — cliente de conexão PostgreSQL
- 🔐 **dotenv** — gerenciamento de variáveis de ambiente

---

## 📦 Requisitos

- **Node.js** `v14` ou superior  
- **npm** (gerenciador de pacotes do Node.js)  
- **PostgreSQL** instalado

---

## 📥 Instalação do Projeto

1. Clone o repositório:

```bash
git clone https://github.com/FelipeGalway/lab-web-2024-2
```

2. Acesse a pasta do projeto:

```bash
cd lab-web-2024-2
```

3. Instale as dependências:

```bash
npm install
```

---

## 🐘 Instalando o PostgreSQL

### Linux:

```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo systemctl status postgresql
```

### macOS:

```bash
brew install postgresql
brew services start postgresql
```

### Windows:

Baixe e instale via: https://www.postgresql.org/download/windows/

Verifique instalação com:

```bash
psql --version
```

---

## 🛠️ Configuração do Banco de Dados

### 1. Criar o banco:

```sql
CREATE DATABASE seu_banco_de_dados;
```

### 2. Criar as tabelas:

Tabela `produto`

```sql
CREATE TABLE produto (
  cod_produto SERIAL PRIMARY KEY,
  nome VARCHAR(100) NOT NULL,
  quantidade INTEGER,
  preco NUMERIC(10, 2)
);
```

Tabela `aluno`

```sql
CREATE TABLE aluno (
  cod_aluno SERIAL PRIMARY KEY,
  nome VARCHAR(100) NOT NULL,
  idade INTEGER
);
```

---

## 🔐 Configuração do .env

Crie um arquivo `.env` na raiz do projeto com os seguintes parâmetros:

```env
PORT=5005
HOST=0.0.0.0

DB_HOST=localhost
DB_PORT=5432
DB_NAME=seu_banco
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
```

---

## ▶️ Scripts de Inicialização

### Produção:

```bash
npm start
```

Executa `node index.js`

### Desenvolvimento (hot-reload):

```bash
npm run dev
```

Utiliza o `--watch` do Node.js para reiniciar o servidor automaticamente em cada alteração

---

## 📚 Dependências Principais

| 📦 Pacote        | 📌 Descrição                            |
|------------------|------------------------------------------|
| `@hapi/hapi`     | Framework web para rotas e APIs          |
| `joi`            | Validação de dados                       |
| `sequelize`      | ORM para PostgreSQL                      |
| `pg`             | Cliente PostgreSQL                       |
| `dotenv`         | Variáveis de ambiente                    |

---

## 🧪 Funcionalidades da API
- Criar, listar, atualizar e excluir produtos

- Criar, listar, atualizar e excluir alunos

- Validação de payload com Joi

- Arquitetura simples e escalável
