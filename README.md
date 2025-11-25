# 💰 Aplicação de Controle Financeiro Pessoal

## Visão Geral do Projeto

Este projeto consiste em uma **API RESTful** para gestão de finanças pessoais, desenvolvida como projeto final da disciplina de Desenvolvimento de Sistemas. O objetivo é fornecer uma API robusta, segura e organizada, seguindo as melhores práticas de arquitetura.

O tema escolhido é **Controle Financeiro Pessoal**, implementando o gerenciamento completo de Transações e Categorias.

---

## ✅ Entregáveis e Requisitos Cumpridos

| Requisito | Detalhamento |
| :--- | :--- |
| **Arquitetura de Software** | **Clean Architecture** (Divisão em Domain, Application, Infrastructure e API). |
| **API para Login (Segurança)** | Implementada com **JWT** (JSON Web Tokens) e *hashing* de senhas com **BCrypt**. |
| **APIs para CRUD Completo** | CRUD implementado para as entidades **Transação** e **Categoria**. |
| **Testes Automatizados** | **6 Casos de Teste (xUnit)** implementados e 100% aprovados no módulo de Autenticação. |
| **Banco de Dados/ORM** | Utilização de **PostgreSQL** em container **Docker** com **Entity Framework Core**. |
| **Tratamento de Erros** | Tratamento de exceções (400, 401, 404, 500) em Controllers e Services. |
| **Swagger** | Documentação completa com esquema de segurança **Bearer (Cadeado)** configurado. |
| **Clean Code** | Código seguindo convenções e princípios de desenvolvimento limpo. |

---

## 🛠️ Tecnologias e Setup

### Tecnologias Principais
* **Linguagem/Framework:** C# (.NET 10)
* **Banco de Dados:** PostgreSQL
* **ORM:** Entity Framework Core
* **Contêiner:** Docker / Docker Compose
* **Testes:** xUnit

### Pré-requisitos
Para rodar a aplicação localmente, você precisa ter:
1.  **Docker Desktop** (para o banco de dados).
2.  **.NET SDK 8.0** instalado.

---

## 🚀 Guia de Uso da API (Endpoints)

### 1. Iniciar a Infraestrutura

Na raiz do projeto (`FinanceiroPessoal/`), execute:

```bash
# Sobe o container PostgreSQL
docker-compose up -d

# Roda o projeto API
dotnet run --project FinanceiroPessoal.Api
2. Acessar a Documentação (Swagger)
Acesse o link no seu navegador (ajuste a porta se necessário): https://localhost:7042/swagger

3. Fluxo de Autenticação (Login/Autorização)
Para usar qualquer rota de CRUD, você deve obter um token:

REGISTRO: Use POST /api/auth/register para criar um novo usuário.

LOGIN: Use POST /api/auth/login para obter o Token JWT.

AUTORIZAÇÃO: Clique no botão Authorize (cadeado) no Swagger e cole o Token no formato: Bearer SEU_TOKEN.

4. Fluxo de Negócio (CRUD e Saldo)
Com o Token aplicado, teste as funcionalidades principais: | Operação | Endpoint | Exemplo | | :--- | :--- | :--- | | Criar Categoria | POST /api/Categories | Criar "Salário" ou "Alimentação". | | Criar Transação | POST /api/Transactions | Registrar uma nova despesa (requer CategoryId). | | Ver Saldo | GET /api/transactions/balance | Retorna o valor total (Receitas - Despesas). |

🧑‍💻 Autores
Este projeto foi desenvolvido em dupla:

Aluno: [Cauê Silva Cabral]

Aluno: [Kauã Gabriel da Silva Antunes]

Link do Repositório: [https://github.com/SEU_USUARIO/FinanceiroPessoal](https://github.com/CaueSC15/FinanceiroPessoal/tree/main)
