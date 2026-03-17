# Testes de API com Postman

Este repositório foi desenvolvido como parte dos meus estudos em **Qualidade de Software**, com foco em **testes de API** utilizando o **Postman**.

Neste projeto, pratiquei a criação e organização de requisições para validar o comportamento da API **Hub de Leitura**, cobrindo fluxos de autenticação, usuários, catálogo de livros e reservas.

A proposta foi construir uma collection simples, mas bem estruturada, com cenários positivos e negativos, validação de status code, mensagens de resposta e uso de variáveis de ambiente para reaproveitamento de dados entre requisições.

## Objetivo do projeto

O objetivo deste projeto foi praticar fundamentos importantes de testes de API, como:

- envio de requisições HTTP;
- organização de testes em collection;
- validação de status code;
- validação de mensagens e regras de negócio;
- uso de variáveis de ambiente;
- reaproveitamento de dados entre requisições;
- cobertura de cenários positivos e negativos.

## Ferramentas utilizadas

- **Postman**
- **API Hub de Leitura**
- **Variáveis de ambiente do Postman**
- **Testes com scripts em JavaScript**

## O que foi desenvolvido

Neste projeto, os testes foram organizados em uma collection única com os seguintes grupos:

- **Autenticação**
- **Usuários**
- **Catálogo de Livros**
- **Reserva de livros - Positivos**
- **Reserva de livros - Negativos**

Essa estrutura foi criada para facilitar a execução dos cenários e tornar a navegação pela collection mais clara.

## Estrutura da collection

```text
Teste de API – Módulo 13
├── Autenticação
│   ├── Login com usuário admin
│   └── Login com usuário padrão
├── Usuários
│   ├── Cadastrar Usuario
│   ├── Listar Usuários
│   ├── Alterar Usuário
│   ├── Listar Usuário por ID
│   └── Deletar Usuário
├── Catalogo de Livros
│   ├── Listar todos os livros disponiveis
│   └── Listar livros usando filtro
├── Reserva de livros - Positivos
│   ├── Criar nova reserva
│   ├── Listar Reservas
│   ├── Atualizar Reserva
│   └── Cancelar Reserva
└── Reserva de livros - Negativos
    ├── Criar nova reserva - bookID Inexistente
    ├── Listar Reservas - Sem Token
    ├── Atualizar Reserva - Sem reservationID
    ├── Cancelar Reserva repetida
    └── Cancelar Reserva - Sem reservationID
```

## Cenários implementados

### Autenticação

- login com usuário administrador;
- login com usuário padrão;
- captura e armazenamento do token para reutilização nas próximas requisições.

### Usuários

- cadastro de usuário;
- listagem de usuários;
- alteração de usuário existente;
- busca de usuário por ID;
- exclusão de usuário.

### Catálogo de Livros

- listagem de livros disponíveis;
- listagem com filtro por categoria e disponibilidade.

### Reservas - Cenários positivos

- criação de nova reserva;
- listagem de reservas;
- atualização de observações da reserva;
- cancelamento de reserva.

### Reservas - Cenários negativos

- tentativa de criar reserva com livro inexistente;
- tentativa de listar reservas sem token;
- tentativa de atualizar reserva sem `reservationId`;
- tentativa de cancelar reserva já cancelada;
- tentativa de cancelar reserva sem `reservationId`.

## Variáveis utilizadas

Durante a execução da collection, foram utilizadas variáveis de ambiente para reaproveitar informações importantes entre as requisições, como:

- `baseUrl`
- `token`
- `userID`
- `bookId`
- `reservationId`

Isso ajudou a encadear melhor os testes e a deixar a execução mais próxima de um fluxo real.

## Validações realizadas

Neste projeto, pratiquei validações como:

- status code das respostas;
- mensagens retornadas pela API;
- presença de campos esperados no body;
- regras de negócio;
- reaproveitamento de IDs e token gerados em etapas anteriores.

## Pré-requisitos

Antes de executar este projeto, é necessário ter:

- **Postman** instalado;
- acesso à API utilizada no exercício;
- um **environment** configurado com a variável `baseUrl`.

## Como executar

1. Importe a collection no Postman.
2. Configure ou selecione o environment com a variável `baseUrl`.
3. Execute as requisições individualmente ou pelo **Runner** do Postman.
4. Siga o fluxo da collection para aproveitar corretamente as variáveis geradas durante os testes.

## O que pratiquei com este projeto

Com este projeto, pratiquei principalmente:

- testes de API com Postman;
- organização de uma collection por fluxo funcional;
- uso de autenticação via token;
- encadeamento de dados entre requisições;
- validação de cenários positivos e negativos;
- validação de mensagens e regras de negócio;
- leitura e interpretação de respostas da API.

## Pontos de melhoria

Como este é um projeto de estudo, ainda existem melhorias que podem ser feitas no futuro, como:

- adicionar mais evidências de execução ao repositório;
- incluir um arquivo de environment de exemplo;
- ampliar a cobertura de cenários negativos;
- documentar melhor o fluxo ideal de execução da collection;
- evoluir parte desses testes para automação em código.

## Considerações finais

Este projeto representa uma etapa importante da minha base em **testes de API**, principalmente no uso do **Postman** para validar fluxos funcionais de forma estruturada.

Meu objetivo aqui foi consolidar fundamentos importantes da área de QA, como organização dos testes, entendimento de requisições HTTP, validação de respostas e reaproveitamento de dados entre etapas do fluxo.

## Autor

**Gustavo Alves Moreno**

Em transição de carreira para a área de **Qualidade de Software**, com foco em testes manuais e automação.

- GitHub: [Guss182](https://github.com/Guss182)

---

Projeto desenvolvido para fins de estudo e prática em testes de API com Postman.
