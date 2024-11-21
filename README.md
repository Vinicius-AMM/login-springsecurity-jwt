<h1 align  = "center">
Projeto Spring Security + JWT
</h1>

API de autenticação e autorização utilizando Spring Security e JWT. 

# Tecnologias
- [Java 21+](https://www.oracle.com/br/java/technologies/downloads/#java21)
- [Docker](https://www.docker.com/products/docker-desktop/)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [JWT](https://jwt.io/introduction)
- [Spring Security](https://spring.io/projects/spring-security)
- [H2 Database](https://www.h2database.com)
- [Postman](https://www.postman.com/downloads/)

# Execução
1. Clonar repositório:
```bash
git clone https://github.com/Vinicius-AMM/login-springsecurity-jwt.git
```
2. Buildar o projeto:
```bash
docker build -t auth-app .
```
3. Executar o container:
```bash
docker run -d -p 8080:8080 --name auth-api auth-app
```
4. Parar Execução:
```bash
docker stop auth-api
```
 
# API Endpoints

Utilizar cliente de requisições HTTP como Insomnia ou Postman.

- Registro:
```bash  
POST http://localhost:8080/auth/register

{
  "name": "Test",
  "email": "test@gmail.com",
  "password": "123456789"
}
```

- Login:
```bash  
POST http://localhost:8080/auth/login
{
  "email": "test@gmail.com",
  "password": "123456789"
}
```

- Informação de autenticação:
```bash  
GET http://localhost:8080/auth/user

Authorization: Bearer {{token}}
```
