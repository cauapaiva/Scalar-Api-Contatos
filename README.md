# ApiContatos10 📱

Uma Web API completa e moderna desenvolvida em **.NET 10** para o gerenciamento e persistência de contatos (CRUD). O projeto simula um ambiente corporativo backend real, utilizando arquitetura desacoplada e integração nativa com banco de dados relacional.

## 🚀 Funcionalidades

O sistema expõe endpoints que permitem realizar as seguintes operações:
*   **Criar Contato (POST):** Registra um novo contato no banco de dados com validação de formato de e-mail em tempo real.
*   **Listar Todos (GET):** Retorna a lista completa de contatos cadastrados.
*   **Buscar por ID (GET):** Localiza um contato específico através de sua chave primária única.
*   **Atualizar (PUT):** Altera dados existentes de um contato cadastrado, validando novamente os campos.
*   **Remover (DELETE):** Exclui de forma definitiva o registro do banco de dados.

## 🛠️ Tecnologias Utilizadas

*   **Linguagem:** C# (.NET 10)
*   **IDE:** Visual Studio 2026
*   **Banco de Dados:** SQL Server
*   **ORM:** Entity Framework Core (Abordagem Code-First com Migrations)
*   **Interface de Testes & Documentação:** Scalar (OpenAPI)

## 📁 Estrutura do Projeto

*   `Controllers/`: Contém o `ContatoController` onde as rotas HTTP e as regras de requisição estão expostas.
*   `Data/`: Concentra o `AppDbContext`, responsável pelo meio de campo entre as classes C# e as tabelas SQL.
*   `Models/`: Contém a classe de entidade `Contato`, mapeando as colunas do banco (ID, Nome, Telefone, E-mail, Endereço e Categoria).

## 🔧 Como Executar o Projeto

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com
   ```
2. **Configurar a String de Conexão:**
   Abra o arquivo `appsettings.json` e altere o parâmetro `Server` para apontar para o nome do seu servidor local do SQL Server.
3. **Executar as Migrations (Console do Gerenciador de Pacotes):**
   ```powershell
   Update-Database
   ```
4. **Rodar a aplicação:**
   Pressione `Ctrl + F5` no Visual Studio e acesse a URL local com o sufixo `/scalar/v1` para interagir com a interface de testes.
