# 🌐 Projeto: API RESTful com Spring Boot e MongoDB (NoSQL)

## 🌟 Visão Geral

Este projeto é uma demonstração prática da construção de uma **API RESTful** utilizando o **Spring Boot** para o *backend* e o **MongoDB** como banco de dados **NoSQL**. O objetivo é criar um serviço de blog ou fórum, focado na persistência de dados não-relacionais e na exploração de consultas flexíveis.

O projeto demonstra a capacidade de integrar tecnologias modernas e de alto desempenho, como o MongoDB, em um ambiente Java/Spring, o que é um diferencial importante no mercado de trabalho.

## 🎯 Destaques Técnicos e Arquitetura

Este projeto ressalta minha experiência com a integração de sistemas e a persistência de dados em ambientes NoSQL:

*   **Spring Boot:** Utilização do *framework* para a criação de uma aplicação *backend* robusta e de fácil manutenção.
*   **MongoDB:** Uso de um banco de dados NoSQL orientado a documentos, ideal para dados com esquemas flexíveis e alta escalabilidade.
*   **Spring Data MongoDB:** Abstração da camada de acesso a dados, utilizando repositórios para operações CRUD e consultas complexas, específicas para o MongoDB.
*   **Modelagem de Dados NoSQL:** Implementação de entidades (`User`, `Post`) e sub-documentos (`Author`, `Comment`) para representar dados de forma desnormalizada, aproveitando a estrutura de documentos do MongoDB.
*   **Consultas Avançadas:** Implementação de *endpoints* com consultas personalizadas, como:
    *   Busca de posts por título contendo um determinado texto (`@Query`).
    *   Busca de posts em um intervalo de datas.
    *   Busca de posts por múltiplos critérios (título e data).
*   **DTOs (Data Transfer Objects):** Uso de DTOs para expor apenas os dados necessários na camada de *resources*, garantindo a segurança e a padronização das respostas da API.
*   **Tratamento de Exceções:** Implementação de tratamento de exceções para lidar com erros de acesso a dados e recursos não encontrados, retornando respostas HTTP consistentes.

## 🛠️ Tecnologias Utilizadas

| Categoria | Tecnologia | Descrição |
| :--- | :--- | :--- |
| **Framework** | Spring Boot | Criação de aplicações Java autônomas e prontas para produção. |
| **Banco de Dados** | MongoDB | Banco de dados NoSQL orientado a documentos. |
| **Persistência** | Spring Data MongoDB | Módulo do Spring para acesso a dados MongoDB. |
| **Linguagem** | Java | Linguagem principal de desenvolvimento. |
| **Build Tool** | Maven | Gerenciamento de dependências. |

## ⚙️ Estrutura do Projeto

O projeto segue a arquitetura em camadas padrão do Spring Boot, adaptada para o MongoDB:

```
.
├── src/main/java/com/devsuperior/workshopmongo/
│   ├── config/             # Configurações iniciais (e.g., Seeding de dados)
│   ├── domain/             # Classes de domínio (Entidades MongoDB)
│   ├── dto/                # Data Transfer Objects (DTOs)
│   ├── repository/         # Interfaces Spring Data MongoDB
│   ├── resources/          # Controllers RESTful (Endpoints)
│   └── services/           # Regras de Negócio
└── ...
```

## 🚀 Como Executar o Projeto

### Pré-requisitos

*   Java Development Kit (JDK) instalado (versão 8 ou superior).
*   Maven instalado.
*   **MongoDB** instalado e rodando localmente (ou acesso a um cluster MongoDB Atlas).

### Configuração

1.  **Configure a Conexão:** No arquivo `application.properties` (ou `application.yml`), configure a URI de conexão com o seu MongoDB:
    ```properties
    spring.data.mongodb.uri=mongodb://localhost:27017/seu_banco_de_dados
    ```

### Passos para Execução

1.  **Clone o Repositório:**
    ```bash
    git clone https://github.com/EduardoJuvenasso/workshop-springboot-mongodb.git
    cd workshop-springboot-mongodb
    ```
2.  **Execute a Aplicação:**
    ```bash
    ./mvnw spring-boot:run
    ```
    A aplicação será iniciada na porta padrão (8080).

### Endpoints Principais (Exemplos)

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `GET` | `/users` | Retorna a lista de todos os usuários. |
| `GET` | `/posts/{id}` | Retorna um post específico por ID. |
| `GET` | `/posts/titlesearch?text=palavra` | Busca posts por título. |
| `GET` | `/posts/fullsearch?text=palavra&minDate=2023-01-01&maxDate=2023-12-31` | Busca posts por texto e intervalo de datas. |

## 💡 Lições Aprendidas e Diversificação

Este projeto demonstra a minha versatilidade em lidar com diferentes paradigmas de persistência de dados:

*   **Transição de Paradigma:** A experiência com MongoDB complementa o conhecimento em bancos de dados relacionais (JDBC e JPA), mostrando a capacidade de escolher a ferramenta certa para o problema (SQL vs. NoSQL).
*   **Modelagem Flexível:** O uso de sub-documentos no MongoDB (como `Author` e `Comment` dentro de `Post`) demonstra a compreensão de como otimizar a leitura de dados em um contexto NoSQL.
*   **Consultas Dinâmicas:** A implementação de consultas com múltiplos critérios e intervalos de datas mostra a habilidade de construir APIs flexíveis e poderosas.

---

*Desenvolvido por Eduardo Juvenasso como parte de um curso acadêmico.*
