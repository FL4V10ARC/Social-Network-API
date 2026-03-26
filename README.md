# Social Network API - Spring Boot + MongoDB

![Java](https://img.shields.io/badge/Java-17-orange?logo=java)
![Spring Boot](https://img.shields.io/badge/SpringBoot-3.x-brightgreen?logo=springboot)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-green?logo=mongodb)
![Maven](https://img.shields.io/badge/Maven-Build-blue?logo=apachemaven)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

REST API desenvolvida com **Java, Spring Boot e MongoDB** que simula uma pequena rede social.
O projeto permite gerenciar **usuários, posts e comentários**, além de realizar **consultas por texto e intervalo de datas** utilizando Spring Data MongoDB.

Este projeto foi desenvolvido com o objetivo de praticar **arquitetura de APIs REST, modelagem de dados orientada a documentos e boas práticas de desenvolvimento backend**.

---

# Tecnologias utilizadas

- Java 17
- Spring Boot
- Spring Data MongoDB
- Maven
- MongoDB
- REST API
- DTO Pattern
- Exception Handling

---

# Arquitetura do Projeto

O projeto segue uma **arquitetura em camadas**, separando responsabilidades para facilitar manutenção e escalabilidade.

src/main/java/com/Flavio/SocialNetworkAPI

config
domain
dto
repository
service
resources (controllers)
exception
util

### Descrição das camadas

**domain**

- Contém as entidades principais do sistema
- Exemplo: `User`, `Post`

**dto**

- Objetos utilizados para transferência de dados
- Evita exposição direta das entidades

**repository**

- Interface de acesso ao banco utilizando **Spring Data MongoDB**

**service**

- Contém a lógica de negócio da aplicação

**resources (controllers)**

- Responsável pelos endpoints da API REST

**exception**

- Tratamento global de exceções da aplicação

---

# Modelo de Dados

## User

- id
- name
- email
- posts

## Post

- id
- date
- title
- body
- author
- comments

## Comment

- text
- date
- author

---

# Funcionalidades da API

## Usuários

- Criar usuário
- Listar usuários
- Buscar usuário por ID
- Atualizar usuário
- Deletar usuário
- Listar posts de um usuário

## Posts

- Buscar post por ID
- Buscar posts por título
- Buscar posts por conteúdo
- Buscar posts por intervalo de datas

## Comentários

- Adicionar comentários em posts

---

# Endpoints principais

## Listar usuários

GET /users

---

## Buscar usuário por ID

GET /users/{id}

---

## Criar usuário

POST /users

Exemplo de requisição:

{
"name": "Maria Brown",
"email": "[maria@gmail.com](mailto:maria@gmail.com)"
}

---

## Atualizar usuário

PUT /users/{id}

---

## Deletar usuário

DELETE /users/{id}

---

## Buscar posts por título

GET /posts/titlesearch?text=viagem

---

## Buscar posts por intervalo de datas

GET /posts/fullsearch?text=viagem&minDate=2018-03-01&maxDate=2018-03-31

---

# Como executar o projeto

## 1 Clonar o repositório

git clone https://github.com/FL4V10ARC//social-network-api.git

---

## 2 Entrar no diretório

cd social-network-api

---

## 3 Configurar MongoDB

Certifique-se que o MongoDB esteja rodando localmente.

Configuração no application.properties:

spring.data.mongodb.uri=mongodb://localhost:27017/workshop_mongo

---

## 4 Executar a aplicação

mvn spring-boot:run

---

## 5 Testar a API

A API estará disponível em:

http://localhost:8080

Exemplo:

http://localhost:8080/users

---

# Aprendizados com o projeto

Durante o desenvolvimento deste projeto foram aplicados conceitos importantes como:

- Desenvolvimento de APIs REST com Spring Boot
- Modelagem de dados com MongoDB
- Uso de DTO para transferência de dados
- Implementação de CRUD completo
- Tratamento global de exceções
- Consultas personalizadas com Spring Data MongoDB

---

# Possíveis melhorias futuras

- Documentação da API com Swagger
- Autenticação com JWT
- Testes unitários com JUnit e Mockito
- Containerização com Docker
- Deploy em Cloud (AWS ou Render)

---

# Autor

Flavio Carvalho

Estudante de Engenharia de Software com foco em **Backend Java, APIs REST e Cloud Computing**.

GitHub:
https://github.com/FL4V10ARC
