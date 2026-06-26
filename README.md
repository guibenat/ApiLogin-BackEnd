# ApiLogin-BackEnd

![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-blue)
![Autenticação](https://img.shields.io/badge/Auth-JWT-orange)
![Licença](https://img.shields.io/badge/Licen%C3%A7a-MIT-green)

Esta é uma API de Autenticação completa e escalável projetada para servir como uma solução robusta de backend para o gerenciamento de usuários, autenticação segura e controle de acesso baseado em tokens **JWT (JSON Web Tokens)**.

O projeto foi construído seguindo os padrões ideais de arquitetura de software, garantindo criptografia segura de senhas, validação estruturada de dados e prevenção contra as principais vulnerabilidades.

---

## 🚀 Funcionalidades Principais

- **Autenticação Segura:** Login estruturado através de tokens JWT com expiração configurável.
- **Gerenciamento de Usuários:** Cadastro de novas credenciais, atualização de dados de perfil e exclusão.
- **Segurança de Dados:** Hashing robusto e seguro para o armazenamento de senhas no banco de dados.
- **Middlewares de Validação:** Filtros integrados para garantir dados limpos, consistentes e sanitizados.
- **Arquitetura Escalável:** Estrutura limpa e desacoplada, facilitando a manutenção e a inserção de novas rotas.

---

## 🛠️ Tecnologias e Ferramentas Típicas

- **Ambiente Back-End:** Node.js / Express ou compatível (C#, Java, Python).
- **Segurança:** `jsonwebtoken` (JWT), criptografia baseada em hashes seguros.
- **Persistência de Dados:** Banco de dados relacional ou não-relacional abstrato via ORM/ODM.

---

## 📦 Configuração e Instalação

### 1. Clonar o Repositório
```bash
git clone [https://github.com/guibenat/ApiLogin-BackEnd.git](https://github.com/guibenat/ApiLogin-BackEnd.git)
cd ApiLogin-BackEnd
2. Configurar Variáveis de AmbienteCrie um arquivo .env na raiz do projeto e preencha-o com suas configurações (utilize o padrão abaixo como referência):Snippet de códigoPORT=5000
DATABASE_URL="sua_string_de_conexao_do_banco"
JWT_SECRET="seu_segredo_super_protegido_e_longo"
JWT_EXPIRES_IN="1d"
3. Instalação e InicializaçãoBash# Instalar as dependências do projeto
npm install

# Executar as migrações/scripts de banco de dados (se aplicável)
npm run db:migrate

# Iniciar o servidor em modo de desenvolvimento
npm run dev
🔌 Endpoints da APIAbaixo estão listadas as principais rotas disponíveis na aplicação:MétodoRotaDescriçãoAutenticaçãoPOST/api/auth/registerCadastra um novo usuário no sistema.PúblicoPOST/api/auth/loginAutentica o usuário e retorna o token JWT.PúblicoGET/api/users/profileRetorna os dados do perfil do usuário logado.Requer Token JWTPUT/api/users/profileAtualiza as informações cadastrais do usuário.Requer Token JWT🔐 Como utilizar o Token JWTPara realizar requisições nas rotas protegidas por autenticação, inclua o token gerado no ato do login dentro do cabeçalho (Header) HTTP de sua requisição utilizando o padrão Bearer:HTTPAuthorization: Bearer <SEU_TOKEN_JWT_AQUI>
Desenvolvido por guibenat.
