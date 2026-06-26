# ApiLogin-BackEnd

![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-blue)
![Autenticação](https://img.shields.io/badge/Auth-JWT-orange)
![Tecnologia](https://img.shields.io/badge/Java-Spring%20Boot-brightgreen)

Esta é uma API de Autenticação robusta e escalável desenvolvida em **Java** com o framework **Spring Boot** (Spring Security). O projeto serve como uma solução completa de backend para o gerenciamento de usuários, autenticação segura e controle de acesso baseado em tokens **JWT (JSON Web Tokens)**.

O projeto foi construído seguindo os padrões ideais de arquitetura e boas práticas de segurança, garantindo criptografia confiável de senhas com BCrypt, validação estruturada de dados e proteção de endpoints.

---

## 🚀 Funcionalidades Principais

- **Autenticação Segura:** Login estruturado através de tokens JWT com expiração configurável.
- **Gerenciamento de Usuários:** Cadastro de novas credenciais, atualização de dados de perfil e exclusão.
- **Segurança de Dados:** Hash de senhas utilizando `BCryptPasswordEncoder` do Spring Security.
- **Validação de Dados:** Uso de anotações do Bean Validation (`@Valid`, `@NotBlank`, etc.) para garantir dados limpos e consistentes.
- **Arquitetura Clean/Modular:** Separação clara em camadas (Controllers, Services, Repositories e Configurações de Segurança).

---

## 🛠️ Tecnologias e Ferramentas

- **Linguagem:** Java (versão 17 ou superior)
- **Framework Principal:** Spring Boot (Spring Web, Spring Security, Spring Data JPA)
- **Segurança:** Gerador e validador de tokens JWT (Java JWT / io.jsonwebtoken)
- **Gerenciador de Dependências:** Maven (ou Gradle)
- **Banco de Dados:** Conexão configurada via JPA/Hibernate com suporte a MySQL, PostgreSQL ou H2.

---

## 📦 Configuração e Instalação

### 1. Clonar o Repositório
```bash
git clone [https://github.com/guibenat/ApiLogin-BackEnd.git](https://github.com/guibenat/ApiLogin-BackEnd.git)
cd ApiLogin-BackEnd
2. Configurar as Propriedades da AplicaçãoAbra o arquivo src/main/resources/application.properties (out application.yml) do projeto e certifique-se de preencher com as suas credenciais de banco de dados e chave do JWT:Propertiesserver.port=8080

# Configurações do Banco de Dados
spring.datasource.url=jdbc:mysql://localhost:3306/seu_banco_de_dados
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update

# Configurações do JWT
api.security.token.secret=seu_segredo_super_protegido_e_longo
3. Compilação e InicializaçãoCertifique-se de ter o JDK instalado. Execute o comando abaixo na raiz do projeto para baixar as dependências e rodar a aplicação:Bash# Limpar e compilar o projeto com o Maven wrapper
./mvnw clean package

# Iniciar a aplicação Spring Boot
./mvnw spring-boot:run
🔌 Endpoints da APIAbaixo estão listadas as principais rotas disponíveis na aplicação:MétodoRotaDescriçãoAutenticaçãoPOST/api/auth/registerCadastra um novo usuário no sistema.PúblicoPOST/api/auth/loginAutentica o usuário e retorna o token JWT.PúblicoGET/api/users/profileRetorna os dados do perfil do usuário logado.Requer Token JWTPUT/api/users/profileAtualiza as informações cadastrais do usuário.Requer Token JWT🔐 Como utilizar o Token JWTPara realizar requisições nas rotas protegidas por autenticação, inclua o token gerado no ato do login dentro do cabeçalho (Header) HTTP de sua requisição utilizando o padrão Bearer:HTTPAuthorization: Bearer <SEU_TOKEN_JWT_AQUI>
Desenvolvido por guibenat.
