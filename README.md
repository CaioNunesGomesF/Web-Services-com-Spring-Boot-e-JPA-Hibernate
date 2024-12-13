# Web Services com Spring Boot e JPA/Hibernate

Bem-vindo ao repositório **Web Services com Spring Boot e JPA/Hibernate**! Este projeto foi desenvolvido como parte do curso **"Java COMPLETO"** oferecido pelo [devsuperior.com.br](https://devsuperior.com.br), ministrado pelo **Dr. Nelio Alves**. A aplicação utiliza **Spring Boot** para criar uma API RESTful e **JPA/Hibernate** para persistência de dados, com um banco de dados em memória H2 para testes e PostgreSQL para produção.

## Tecnologias 🚀

- **Java 17** (Versão recomendada)
- **Spring Boot 2.x** (Framework para construção de aplicações Java)
- **Spring Data JPA** (Persistência de dados com JPA e Hibernate)
- **H2 Database** (Banco de dados em memória para testes)
- **PostgreSQL** (Banco de dados para produção)
- **Heroku** (Plataforma de deployment)
- **Maven** (Gerenciador de dependências)
- **JPA** (Java Persistence API)
- **JWT (JSON Web Token)** para autenticação

## Funcionalidades 🎯

Esse projeto é uma API RESTful para o gerenciamento de **usuários**, **pedidos** e **produtos** com as seguintes funcionalidades:

- **CRUD de Usuários** (Create, Read, Update, Delete)
- **Cadastro de Pedidos** com relação a produtos e usuários
- **Cadastro de Produtos e Categorias**
- **Exceções personalizadas** para tratamento de erros (`ResourceNotFoundException`, `DatabaseException`)
- **Autenticação JWT** para acesso seguro

## Instalação 🔧

Para rodar o projeto localmente, siga os passos abaixo:

1. **Clone o repositório:**
    ```bash
    git clone https://github.com/CaioNunesGomesF/Web-Services-com-Spring-Boot-e-JPA-Hibernate.git
    cd Web-Services-com-Spring-Boot-e-JPA-Hibernate
    ```

2. **Configure o PostgreSQL (para produção):**
    - Se for utilizar PostgreSQL, crie um banco de dados chamado `springboot_course` e configure o arquivo `application-dev.properties` com as credenciais do banco.

3. **Execute o projeto:**
    - No terminal, execute:
    ```bash
    ./mvnw spring-boot:run
    ```

    O servidor estará disponível em [http://localhost:8080](http://localhost:8080).

4. **Banco de dados H2 para testes:**
    - O banco de dados H2 estará acessível em [http://localhost:8080/h2-console](http://localhost:8080/h2-console) com a URL `jdbc:h2:mem:testdb`.

## Exemplo de Requisição 📝

### Inserir Usuário:

```json
{
  "name": "Bob Brown",
  "email": "bob@gmail.com",
  "phone": "977557755",
  "password": "123456"
}
```
## Estrutura do Projeto 🏗️

O projeto segue uma arquitetura baseada em camadas:

- **Controller (Resource):** Expõe os endpoints da API.
- **Service:** Contém a lógica de negócio.
- **Repository:** Interage diretamente com o banco de dados.

## Exceções e Tratamento de Erros ⚠️

O projeto implementa o tratamento de erros com exceções personalizadas, como `ResourceNotFoundException` e `DatabaseException`, para garantir que a API responda adequadamente a falhas.

### Exemplo de código para tratamento de exceções:

```java
// ResourceNotFoundException.java
public class ResourceNotFoundException extends RuntimeException {
    public ResourceNotFoundException(String message) {
        super(message);
    }
}
```
## Agradecimentos 🙏

Gostaria de agradecer ao professor **Dr. Nelio Alves** do [devsuperior.com.br](https://devsuperior.com.br) pela excelente formação e conteúdo do curso, que ajudou a construir este projeto.

