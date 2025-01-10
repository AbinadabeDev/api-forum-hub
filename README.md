# ForumHub API

Bem-vindo ao **ForumHub**, uma API RESTful desenvolvida com **Spring Boot** para gerenciar fóruns, postagens e usuários com segurança e eficiência. Esta API oferece funcionalidades completas para autenticação, criação, listagem, atualização e exclusão de tópicos, além de integrações com Swagger para documentação interativa.

## 📋 Funcionalidades

### **Postagens**
- **Criar Tópico**: Cadastro de novas postagens no fórum.
- **Listar Tópicos**:
  - Listagem paginada de todas as postagens.
  - Top 10 tópicos mais recentes.
  - Busca de tópicos por curso e ano.
- **Visualizar Tópico Específico**: Detalhamento de uma postagem específica por ID.
- **Atualizar Tópico**: Alteração de conteúdo de postagens existentes.
- **Excluir Tópico**: Remoção definitiva de tópicos.

### **Usuários**
- **Autenticação**:
  - Login com geração de token JWT.
  - Gerenciamento seguro de sessões.

---

## 🚀 Tecnologias Utilizadas
- **Java 17**
- **Spring Boot 3.0+**
- **Spring Security** (com JWT para autenticação)
- **Hibernate/JPA** (persistência de dados)
- **PostgreSQL** (banco de dados relacional)
- **Swagger/OpenAPI** (documentação interativa)
- **Maven** (gerenciamento de dependências)

---

## 🛠️ Instalação e Execução

### **Pré-requisitos**
- **Java 17** ou superior
- **Maven** instalado
- Banco de dados **PostgreSQL** configurado

### **Passos**
1. Clone este repositório:
   ```bash
   git clone https://github.com/abinadabedev/forumhub-api.git
   cd forumhub-api
   ```

2. Configure o banco de dados no arquivo `application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/forumhub
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   ```

3. Compile o projeto:
   ```bash
   mvn clean install
   ```

4. Execute a aplicação:
   ```bash
   mvn spring-boot:run
   ```

5. Acesse a API:
    - Base URL: `http://localhost:8080`
    - Swagger UI: `http://localhost:8080/swagger-ui.html`

---

## 🗂️ Endpoints Principais

### **Postagem**
- **POST** `/topicos`  
  Criar um novo tópico.

- **GET** `/topicos`  
  Listar todas as postagens (com paginação).

- **GET** `/topicos/top10`  
  Retornar os 10 tópicos mais recentes.

- **GET** `/topicos/buscar-ano-data`  
  Buscar postagens por curso e ano.

- **GET** `/topicos/{id}`  
  Buscar detalhes de uma postagem específica.

- **PUT** `/topicos`  
  Atualizar uma postagem existente.

- **DELETE** `/topicos/{id}`  
  Remover uma postagem.

### **Usuários**
- **POST** `/login`  
  Autenticar e obter um token JWT.

---

## 🔐 Segurança
Esta API utiliza **Spring Security** com autenticação via **JWT (JSON Web Token)**. Para acessar os endpoints protegidos, inclua o token no cabeçalho da requisição:

```http
Authorization: Bearer <seu_token_jwt>
```

---

## 🤝 Contribuição
Contribuições são sempre bem-vindas!
1. Faça um fork do repositório.
2. Crie uma branch para sua feature: `git checkout -b minha-feature`.
3. Realize suas alterações e faça commit: `git commit -m 'Minha nova feature'`.
4. Envie para o repositório: `git push origin minha-feature`.
5. Abra um Pull Request.

---

## 📝 Licença
Este projeto está sob a licença **MIT**. Sinta-se à vontade para utilizá-lo e modificá-lo conforme necessário.

---

## 📧 Contato
Desenvolvido por [Abinadabe Oliveira](https://github.com/abinadabedev).  
Caso tenha dúvidas ou sugestões, entre em contato:
- **E-mail**: abinadabedev@gmail.com
- **LinkedIn**: [linkedin.com/in/abinadabeoliveira](https://linkedin.com/in/abinadabeoliveira)
```