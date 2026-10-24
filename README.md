# MercadoVivaVendas

## Descrição do Projeto

O MercadoVivaVendas é um sistema desenvolvido em Java com o objetivo de auxiliar no gerenciamento de produtos, estoque e vendas de um estabelecimento comercial.

A aplicação funciona por meio de uma interface de linha de comando, permitindo que o usuário realize operações de cadastro, consulta e listagem de informações de maneira simples e organizada.

O projeto foi desenvolvido com a finalidade de aplicar conceitos fundamentais de programação orientada a objetos, organização de classes, estruturas condicionais, estruturas de repetição e manipulação de dados em Java.

## Funcionalidades

### Gerenciamento de Estoque

O módulo de estoque permite cadastrar produtos, consultar informações e visualizar os produtos registrados no sistema.

O usuário pode cadastrar produtos informando seu identificador, nome e preço. Também é possível listar os produtos cadastrados e realizar buscas utilizando o identificador do produto.

Na implementação atual, o sistema permite armazenar até três produtos durante a execução.

### Gerenciamento de Vendas

O módulo de vendas permite registrar e consultar informações relacionadas às operações comerciais.

Cada venda contém informações como identificador do produto, nome, preço, valor total e forma de pagamento.

O sistema permite cadastrar vendas, listar os registros realizados e buscar vendas pelo identificador do produto.

Na implementação atual, o sistema permite registrar até três vendas durante a execução.

### Menu Principal

O sistema possui um menu interativo que permite ao usuário acessar os módulos de estoque e vendas.

A navegação é realizada por meio de opções numéricas, utilizando estruturas condicionais e de repetição para controlar o funcionamento da aplicação.

### Cadastro de Clientes

O projeto possui uma classe destinada à representação de clientes, contendo informações como identificador, nome, CPF e telefone.

Essa classe faz parte da estrutura de modelos do sistema, mas ainda não está integrada ao menu principal.

## Tecnologias Utilizadas

**Java:** Linguagem de programação utilizada no desenvolvimento do sistema.

**Programação Orientada a Objetos:** Paradigma utilizado para organizar as classes, os atributos e os métodos da aplicação.

**Java Scanner:** Classe utilizada para receber informações fornecidas pelo usuário por meio do terminal.

**Java Console:** Interface textual utilizada para interação com o sistema.

## Estrutura do Projeto

O código está dividido em pacotes responsáveis pela representação dos dados, pelas regras de funcionamento e pela inicialização da aplicação.

```text
br/com/mercadojava/
│
├── app/
│   └── MercadoApp.java
│
├── modelo/
│   ├── Cliente.java
│   ├── Produto.java
│   └── Venda.java
│
└── servico/
    ├── GerenciadorDeEstoque.java
    └── GerenciadorDeVendas.java
```

### Organização das Classes

**MercadoApp.java**

Classe principal responsável pela inicialização do sistema e pela apresentação do menu de navegação.

**Cliente.java**

Classe responsável pela representação dos dados de um cliente, incluindo identificador, nome, CPF e telefone.

**Produto.java**

Classe responsável pela representação dos produtos, contendo identificador, nome e preço.

**Venda.java**

Classe responsável pela representação das vendas. Herda os atributos da classe Produto e acrescenta informações sobre o valor total e a forma de pagamento.

**GerenciadorDeEstoque.java**

Classe responsável pelas operações de cadastro, listagem e consulta de produtos.

**GerenciadorDeVendas.java**

Classe responsável pelas operações de cadastro, listagem e consulta de vendas.

## Conceitos Aplicados

### Programação Orientada a Objetos

O sistema utiliza classes e objetos para representar os elementos relacionados ao gerenciamento comercial.

### Encapsulamento

Os atributos das classes são declarados como privados, permitindo o acesso controlado às informações por meio de métodos públicos.

### Herança

A classe Venda utiliza herança da classe Produto, reaproveitando atributos e métodos relacionados às informações dos produtos.

### Estruturas Condicionais

São utilizadas estruturas como `if`, `else` e `switch` para controlar as opções selecionadas pelo usuário.

### Estruturas de Repetição

O sistema utiliza estruturas como `do while` e `while` para manter os menus ativos e validar determinadas entradas.

### Tratamento de Exceções

O módulo de vendas utiliza tratamento de exceções para identificar entradas numéricas inválidas durante o cadastro e a consulta de informações.

## Requisitos para Execução

Para executar o projeto, é necessário possuir o Java Development Kit (JDK) instalado e configurado.

O código pode ser executado por meio de uma IDE compatível com Java, como IntelliJ IDEA, Eclipse ou Visual Studio Code, ou diretamente pelo terminal.

## Como Executar o Projeto

### 1. Obter o Projeto

Clone o repositório utilizando o Git:

```bash
git clone URL_DO_REPOSITORIO
```

Também é possível baixar o projeto em formato ZIP e extrair os arquivos.

### 2. Organizar os Arquivos

Certifique-se de que os arquivos Java estejam organizados conforme os pacotes declarados no código.

Os arquivos disponibilizados originalmente precisam ser salvos com seus respectivos nomes de classe e a extensão `.java`.

### 3. Compilar o Projeto

Acesse a pasta que contém o diretório `br` e execute:

```bash
javac br/com/mercadojava/modelo/*.java br/com/mercadojava/servico/*.java br/com/mercadojava/app/*.java
```

### 4. Executar a Aplicação

Após a compilação, execute:

```bash
java br.com.mercadojava.app.MercadoApp
```

O menu principal será apresentado no terminal.

## Exemplo de Utilização

Ao iniciar a aplicação, o usuário visualizará o seguinte menu:

```text
=== BEM-VINDO AO SISTEMA MERCADOJAVA ===

1. Acessar Gestão de Estoque
2. Acessar Gestão de Vendas
3. Sair do Sistema

Escolha uma opção:
```

Ao selecionar a opção de gerenciamento de estoque, será apresentado:

```text
=== SISTEMA DE GESTÃO DE ESTOQUE ===

1. Cadastrar produto
2. Listar produtos
3. Buscar produto por ID
4. Sair
```

Ao selecionar a opção de gerenciamento de vendas, será apresentado:

```text
=== SISTEMA DE GESTÃO DE VENDAS ===

1. Cadastrar venda
2. Listar vendas
3. Buscar venda por ID do produto
4. Sair
```

## Limitações Atuais

O sistema utiliza armazenamento temporário em memória, não possuindo integração com banco de dados.

Os registros de produtos e vendas são perdidos quando a aplicação é encerrada.

O gerenciamento de estoque e o gerenciamento de vendas possuem limite de três registros cada.

O cadastro de clientes está representado no código, mas ainda não possui funcionalidades disponíveis no menu principal.

## Possíveis Melhorias

### Integração com Banco de Dados

Implementação de persistência de dados para armazenar informações de produtos, clientes e vendas.

### Ampliação do Cadastro

Substituição do limite fixo de registros por coleções dinâmicas, permitindo cadastrar uma quantidade maior de produtos e vendas.

### Gerenciamento de Clientes

Implementação de funcionalidades para cadastro, listagem, atualização e exclusão de clientes.

### Controle de Quantidade em Estoque

Implementação de controle de unidades disponíveis, incluindo atualização automática após a realização de vendas.

### Relatórios de Vendas

Desenvolvimento de relatórios para acompanhamento de faturamento, movimentações comerciais e produtos vendidos.

## Objetivo do Projeto

O principal objetivo do MercadoVivaVendas é demonstrar a aplicação prática de conceitos fundamentais da linguagem Java no desenvolvimento de um sistema de gerenciamento comercial.

O projeto permite exercitar a organização de classes, a utilização de métodos, o encapsulamento, a herança, o tratamento de entradas e a implementação de menus interativos.

## Status do Projeto

Projeto acadêmico com funcionalidades básicas de gerenciamento de estoque e vendas implementadas, podendo receber melhorias e novas funcionalidades.

## Considerações Finais

O MercadoVivaVendas apresenta uma implementação inicial de um sistema de gerenciamento comercial, reunindo funcionalidades essenciais para cadastro e consulta de produtos e vendas.

Seu desenvolvimento contribui para a compreensão dos fundamentos da programação orientada a objetos e para a aplicação de boas práticas de organização de código em Java.
