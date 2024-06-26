# meat-backend

# Projeto Meat

Este é um projeto Spring Boot que exemplifica a criação de um CRUD simples para gerenciamento de usuários.

## Índice

- [Instalação](#instalação)
- [Dependências](#dependências)
- [Configuração](#configuração)
- [Endpoints da API](#endpoints-da-api)
- [Swagger UI](#swagger-ui)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Instalação

Para instalar e executar este projeto, siga os passos abaixo:

1. Clone o repositório:
    ```sh
    git clone https://github.com/jairobmiranda/meat-backend.git
    cd projeto-meat
    ```

2. Compile e execute o projeto usando Maven:
    ```sh
    mvn clean install -DskipTests
    mvn spring-boot:run
    ```

## Dependências

O projeto utiliza as seguintes dependências principais:

- Spring Boot Starter Data JPA
- Spring Boot Starter Web
- Spring Boot DevTools
- MariaDB Java Client
- SpringDoc OpenAPI UI

Todas as dependências estão listadas no arquivo `pom.xml`.

## Configuração

1. Configure as propriedades do banco de dados no arquivo `application.properties`:
    ```properties
    spring.datasource.url=jdbc:mariadb://localhost:3306/meat
    spring.datasource.username=seu_usuario
    spring.datasource.password=sua_senha
    spring.jpa.hibernate.ddl-auto=update
    spring.datasource.driver-class-name=org.mariadb.jdbc.Driver
    ```

2. Certifique-se de que o MariaDB está rodando e acessível nas configurações fornecidas.

## Endpoints da API

A API possui os seguintes endpoints:

- **Criar Usuário**
    ```http
    POST /usuarios
    ```
    - Corpo da requisição:
        ```json
        {
            "nome": "Nome do Usuário",
            "dataNascimento": "2000-01-01"
        }
        ```

- **Listar Usuários**
    ```http
    GET /usuarios
    ```

- **Buscar Usuário por ID**
    ```http
    GET /usuarios/{id}
    ```

## Swagger UI

Você pode visualizar e testar os endpoints da API usando o Swagger UI. Após iniciar a aplicação, acesse:

