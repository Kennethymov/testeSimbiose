# Projeto realizado para fase Teste da Simbiose

Consiste em um CRUD dos seguintes dados referentes a uma pessoa: nome, email, data de nascimento. 

* Construída com Node.js, Express, Typescript, Sequelize com MySQL e Docker
* Utilizando as práticas do REST
* Aplicada Arquitetura de Software, com as camadas de Modelo, de Serviço e de Controladores


### Instruções

- Para rodar o repositório localmente, realize o clone do projeto e utilize os comandos a seguir para inicializar o Docker, instalar as dependências e configurar o banco de dados:

```
docker-compose up --build
docker-compose down // para parar completamente a aplicação
```

### Endpoints

#### Usuário

| Método | Funcionalidade | URL |
|---|---|---|
| `POST` | Cria um novo usuário e retorna o usuário cadastrado  | http://localhost:3001/pessoa |
| `GET` | Retorna todas os usuários cadastrados | http://localhost:3001/pessoas |
| `GET` | Retorna os dados de um usuário específico | http://localhost:3001/pessoa/:id |
| `PUT` | Atualiza os dados de um usuário específico | http://localhost:3001/pessoa/:id |
| `DELETE` | Deleta os dados do usuário através da informação do token | http://localhost:3001/pessoa/:id |


Na requisição POST, é necessário informar todos os dados do usuário no formato a seguir:

```
{
  "name": "Usuário Exemplo",
  "email": "usuario-exemplo@email.com",
  "birthDate": "YYYY-MM-DD"
}
```

Na requisição PUT, é necessário informar pelo menos um dos dados do usuário no formato a seguir:

```
{
  "name": "Usuário Exemplo",
  "email": "usuario-exemplo@email.com",
  "birthDate": "YYYY-MM-DD"
}
```