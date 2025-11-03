# 🚧 Algatransito API — Em Construção 🚧

> API desenvolvida durante os estudos de **Java + Spring Boot** pela [AlgaWorks](https://www.algaworks.com/), com foco em boas práticas, arquitetura REST, versionamento de banco de dados e testes automatizados.

---

## 🧭 Visão Geral

O **Algatransito API** é uma aplicação REST que gerencia entidades relacionadas a um sistema de trânsito, como **proprietários, veículos e infrações**, seguindo padrões de **clean code**, **DDD simplificado** e **migrações Flyway** para controle de esquema.

Atualmente o projeto está **em fase de construção**, com foco em:

- Estruturar a base do projeto Spring Boot
- Configurar persistência com JPA e Flyway
- Implementar endpoints REST padronizados
- Escrever testes automatizados
- Validar respostas via **Postman**
- Preparar integração contínua (CI/CD)

---

## ⚙️ Stack Técnica

| Tecnologia | Descrição |
|-------------|------------|
| ☕ **Java 17+** | Linguagem principal |
| 🌱 **Spring Boot 3.x** | Framework para criação da API |
| 🧩 **Spring Data JPA** | Acesso e persistência de dados |
| 🧱 **Flyway** | Migrações e versionamento de banco |
| 🐬 **MySQL** | Banco de dados relacional |
| 🧪 **JUnit 5** | Testes unitários e de integração |
| 📦 **Maven 3.9+** | Gerenciador de build e dependências |
| 💡 **Lombok** | Redução de boilerplate |
| 🧰 **Postman** | Testes e validação manual dos endpoints |
| 🐳 **Docker** *(em breve)* | Empacotamento e execução isolada |

---

## 🧩 Estrutura do Projeto
algatransito-api/
├── src/
│ ├── main/
│ │ ├── java/com/algaworks/algatransito/ # Código-fonte principal
│ │ └── resources/
│ │ ├── application.properties # Configurações
│ │ └── db/migration/ # Scripts Flyway (V001__, V002__, etc)
│ └── test/java/... # Testes automatizados
├── pom.xml # Configuração Maven
└── README.md



---

## ▶️ Como Executar Localmente

### 🧰 Pré-requisitos

- ☕ **Java 17+**
- 🐬 **MySQL 8+** (ou Docker)
- 📦 **Maven 3.9+**
- 🧰 **Postman** (para testar a API)

---

### ⚙️ Configuração do Banco de Dados

1. Crie o banco:
   ```sql
   CREATE DATABASE algatransito;
   src/main/resources/application.properties

   Exemplo:
spring.datasource.url=jdbc:mysql://localhost:3306/algatransito?createDatabaseIfNotExist=true&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=1234
spring.jpa.hibernate.ddl-auto=none
spring.flyway.enabled=true


▶️ Rodando o Projeto
# Clone o repositório
git clone git@github.com:WilliamD2022/algatransito-api.git

# Entre no diretório
cd algatransito-api

# Execute o build
mvn clean package

# Rode o projeto
mvn spring-boot:run


A API iniciará em:
👉 http://localhost:8080

🧪 Testando com o Postman

Você pode testar os endpoints usando o Postman.

🔹 Importar Collection

Abra o Postman

Clique em Import → Link ou File

Importe o arquivo de collection (em breve será disponibilizado no repositório em docs/postman_collection.json)

🔹 Exemplo de Requisição

GET /proprietarios

curl -X GET http://localhost:8080/proprietarios


POST /proprietarios

curl -X POST http://localhost:8080/proprietarios \
  -H "Content-Type: application/json" \
  -d '{
        "nome": "William Domingues",
        "telefone": "11999999999"
      }'

🗂️ Migrações Flyway

Scripts versionados ficam em:

src/main/resources/db/migration/


Exemplo:

V001__cria-tabela-proprietario.sql
V002__renomeia-coluna-telefone.sql

📅 Próximos Passos

 Criar endpoints REST completos (CRUD de Proprietário e Veículo)

 Criar collection Postman com exemplos de chamadas

 Configurar Swagger/OpenAPI

 Adicionar Testcontainers para testes de integração

 Criar pipeline CI/CD (GitHub Actions)

 Empacotar com Docker e publicar no AWS ECS

🧑‍💻 Autor

William Domingues Barbosa
📍 Atibaia - SP
🚀 Engenheiro de Software | QA Automation | DevOps | Java & AWS
🔗 LinkedIn

💻 GitHub

💡 Projeto educacional baseado nos estudos da formação Java e Spring Boot da AlgaWorks. Em constante evolução.


---

### 💾 Como aplicar
No terminal:

```bash
echo "<cole o conteúdo acima>" > README.md
git add README.md
git commit -m "docs: adiciona README com instruções de execução e uso do Postman"
git push





