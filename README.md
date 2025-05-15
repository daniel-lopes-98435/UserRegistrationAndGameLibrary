# ?? FIAP Cloud Games - API de Cadastro e Biblioteca de Jogos

Este projeto � a entrega da **Fase 1** do Tech Challenge da FIAP e consiste em uma **API RESTful desenvolvida em
.NET 8** para gerenciar o **cadastro de usu�rios** e sua **biblioteca de jogos adquiridos**.
Essa API � o ponto de partida para uma plataforma robusta de games voltada � educa��o em tecnologia.

---

## ?? Objetivo

Criar um MVP funcional, utilizando arquitetura limpa, boas pr�ticas de desenvolvimento, persist�ncia de dados com Entity Framework Core 
e autentica��o com JWT, que sirva como base s�lida para as pr�ximas fases do projeto.

---

## ??? Tecnologias Utilizadas

- .NET 8 (ASP.NET Core MVC)
- Entity Framework Core + Migrations
- Docker (para PostgreSQL)
- JWT Authentication & Authorization
- xUnit + Moq para testes unit�rios
- Testes automatizados
- Swagger (Swashbuckle)
- Domain-Driven Design (DDD)
- Middlewares personalizados (log e tratamento de exce��es)

---

## ?? Funcionalidades

### ? Cadastro e Gerenciamento de Usu�rios
- Cadastro com nome, e-mail e senha segura
- Valida��o de e-mail e senha forte
- Atualiza��o e exclus�o de usu�rios
- Filtro por nome ou e-mail

### ?? Autentica��o e Permiss�es
- Login com gera��o de token JWT
- Controle de acesso por roles (`Admin`, `User`)
- Permiss�es separadas em entidade `UserAuthorization` (relacionamento 1:1)

### ?? Biblioteca de Jogos
- Associa��o de jogos a usu�rios
- Listagem de jogos adquiridos por usu�rio
- Exclus�o de jogos da biblioteca

---

## ?? Arquitetura
?? UserRegistrationAndGameLibrary
??? ?? Api # Controllers, Middlewares, Program.cs
??? ?? Application # DTOs, Interfaces de Servi�o
??? ?? Domain # Entidades, Enums, Value Objects
??? ?? Infra # DbContext, Migrations, Reposit�rios

- Arquitetura em camadas com separa��o clara de responsabilidades
- Uso de DDD e boas pr�ticas REST
- Inje��o de depend�ncia configurada com `AddScoped`

---

### ? Passos

1. Clone o reposit�rio:
```bash
git clone https://github.com/leticiacarolinesilva/UserRegistrationAndGameLibrary.git

2. Caso n�o tenha o postgreSQL instalado voc� pode iniciar um container PostgreSQL localmente com o seguinte comando:

```bash
docker run --name meu-postgres \
  -p 5432:5432 \
  -e POSTGRES_USER=gameuser \
  -e POSTGRES_PASSWORD=gamepassword \
  -e POSTGRES_DB=gameplatform \
  -d postgres

  3. Execute o projeto

  4. Acesse o Swagger: https://localhost:7213/swagger


