

# CRUD de Produtos - Spring Boot

Projeto simples de uma API REST para cadastro de produtos, desenvolvido com Java 24 e Spring Boot 3.5.4. Implementa operações básicas de CRUD (Create, Read, Update, Delete), com persistência em banco de dados PostgreSQL e versionamento de schema com Flyway.

## Tecnologias utilizadas

- Java 24
- Spring Boot 3.5.4
- Spring Web
- Spring Data JPA
- PostgreSQL
- Flyway
- Maven

## Estrutura do Projeto

```

src/
├── controller   # Camada REST - endpoints da API
├── dtos         # Data Transfer Objects
├── model        # Entidades JPA
├── repository   # Interface de acesso a dados
└── CrudApplication.java # Classe principal (main)

````

## Endpoints

| Método | Rota          | Descrição                  |
|--------|---------------|----------------------------|
| GET    | /products     | Lista todos os produtos    |
| GET    | /products/{id}| Busca produto por ID       |
| POST   | /products     | Cria um novo produto       |
| PUT    | /products/{id}| Atualiza um produto        |
| DELETE | /products/{id}| Remove um produto          |

## Exemplo de Payload (POST/PUT)

```json
{
  "name": "Produto Exemplo",
  "price": 1000
}
````

## Como executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/seu-usuario/crud-produtos-spring.git
   cd crud-produtos-spring
   ```

2. Configure o `application.properties` com seu banco PostgreSQL.

3. Execute a aplicação:

   ```bash
   ./mvnw spring-boot:run
   ```

4. Acesse a API em: `http://localhost:8080/products`

---
**Obs.:** O projeto utiliza Flyway para versionamento do banco. Certifique-se de que o schema esteja acessível para que as migrations sejam aplicadas corretamente.



