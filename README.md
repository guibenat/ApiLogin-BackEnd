# ApiString 🔐

![Status do Projeto](https://img.shields.io/badge/status-em_desenvolvimento-yellow)
![Java](https://img.shields.io/badge/Java-17%2B-orange?logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-green?logo=spring)
![Spring Security](https://img.shields.io/badge/Spring_Security-Protected-6DB33F?logo=springsecurity)

Uma API REST de autenticação e controle de acesso robusta, desenvolvida em **Java** com o ecossistema **Spring**. O projeto gerencia o fluxo de login, criação de usuários e proteção de rotas de forma segura.

---

## 🛠️ Tecnologias e Dependências Utilizadas

O projeto foi estruturado utilizando as seguintes tecnologias do ecossistema Spring:

* **Java 17+** (ou a versão que você estiver usando)
* **Spring Boot:** Framework base para a construção da API.
* **Spring Security:** Responsável pela autenticação, autorização e proteção contra vulnerabilidades.
* **Spring Data JPA:** Abstração de persistência de dados e mapeamento objeto-relacional (ORM).
* **Banco de Dados Local:** Configurado para persistência local em ambiente de desenvolvimento (ex: H2, PostgreSQL ou MySQL local).

---

## 🚀 Como Executar o Projeto Localmente

### Pré-requisitos
Antes de começar, certifique-se de ter instalado em sua máquina:
* **JDK 17** ou superior.
* **Maven** (gerenciador de dependências).
* Uma IDE de sua preferência (IntelliJ IDEA, Eclipse, VS Code).
* O serviço do seu Banco de Dados ativo localmente (caso não esteja usando o H2 em memória).

### Passo a Passo

1. **Clone o repositório:**
```bash
   git clone [https://github.com/guibenat/ApiString.git](https://github.com/guibenat/ApiString.git)
