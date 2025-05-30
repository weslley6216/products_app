# Products App

Este projeto é uma aplicação de gestão de produtos construída com Ruby on Rails (API) e ReactJS (Frontend) e orquestrada via Docker Compose.

## Propósito

Fornecer uma plataforma completa para o gerenciamento de produtos, com as funcionalidades de cadastro, listagem, atualização e remoção de produtos (CRUD).

## Arquitetura

O projeto é composto por três partes principais:

* **[Products API](https://github.com/weslley6216/products_api):**
  * Uma API RESTful construída com Ruby on Rails, responsável pela lógica de negócios, validações e persistência de dados.
* **[Products Frontend](https://github.com/seu-usuario/product_frontend):**
  * Uma aplicação web construída com ReactJS, que fornece a interface de usuário para interação com os produtos.
* **Products App:**
  * Este repositório, que orquestra a execução da API e do Frontend utilizando Docker Compose.

O fluxo de dados é o seguinte:

1. O frontend se comunica com a API para todas as operações de CRUD (Criar, Ler, Atualizar, Excluir) de produtos.
2. O backend processa as requisições, interage com o banco de dados e retorna os dados dos produtos, incluindo também o atributo `missing_letter` calculado.

## Configuração e Execução

1. **Certifique-se de ter o Docker instalado localmente.**
2. **Clone este repositório:**

    ```bash
    git clone git@github.com:weslley6216/products_app.git
    ```

3. **Navegue até o diretório do projeto:**

    ```bash
    cd products_app
    ```

4. **Copie o arquivo `.env.example` para `.env`** para configurar as variáveis de ambiente necessárias (ex: credenciais do banco de dados, portas, etc.):

    ```bash
    cp .env.example .env
    ```

6. **Execute o projeto com Docker Compose:**

    ```bash
    docker compose up
    ```

## Acessando a Aplicação

Após os serviços subirem, abra o navegador e acesse:

```bash
http://localhost:4000
```

## Comandos Adicionais

Após rodar um `docker compose up`, abra uma nova instância no terminal e execute um dos passos abaixo:

* **Executar testes RSpec (Product API):**

    ```bash
    docker compose exec backend rspec
    ```

* **Abrir um shell Bash na API:**

    ```bash
    docker compose exec backend bash
    ```

* **Abrir um shell Sh no Frontend:**

    ```bash
    docker compose exec frontend sh
    ```

---

## Informações Adicionais

Para obter informações detalhadas sobre dependências de desenvolvimento, endpoints da API, tecnologias do frontend e testes, consulte os READMEs específicos de cada projeto:

* **[Products API](https://github.com/weslley6216/products_api)**
* **[Products Frontend](https://github.com/weslley6216/products_frontend)**
