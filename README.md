# Burger Queen (API Client)

## Índice

* [1. Prefácio](#1-prefácio)
* [2. Resumo do projeto](#2-resumo-do-projeto)
* [3. Objetivos de aprendizagem](#3-objetivos-de-aprendizagem)
* [4. Considerações gerais](#4-considerações-gerais)
* [5. Critérios de aceitação mínimos do projeto](#5-critérios-de-aceitação-mínimos-do-projeto)
* [6. Implantação](#6-implantação)
* [7. Pistas, tips e leituras complementares](#7-pistas-tips-e-leituras-complementares)
* [8. Funcionalidades opcionais](#8-funcionalidades-opcionais)

***

## 1. Prefácio

[React](https://pt-br.react.dev/) e [Angular](https://angular.io/)
são alguns dos _frameworks_ e _bibliotecas_ de JavaScript mais usados
na área de desenvolvimento ao redor do mundo e existe uma razão para isso.
No contexto do navegador, [_manter a interface sincronizada com o estado é
difícil_](https://medium.com/dailyjs/the-deepest-reason-why-modern-javascript-frameworks-exist-933b86ebc445).
Ao eleger um _framework_ ou _biblioteca_ para nossa interface, nos apoiamos em
uma série de convenções e implementações _testadas_ e _documentadas_ para
resolver um problema comum a toda interface web. Isto nos permite concentrar
melhor (dedicar mais tempo) nas características _específicas_ de nossa
aplicação.

Quando escolhemos uma destas tecnologias não só importamos um pedaço de código
para reusar (o qual já é um grande valor por si só), mas também adotamos uma
**arquitetura**, uma série de **princípios de design**, um paradigma, algumas
**abstrações**, um **vocabulário**, uma **comunidade**, etc.

Como desenvolvedora Front-End, estes kits de desenvolvimento podem resultar em
uma grande ajuda para implementar rapidamente características dos projetos em que
você for trabalhar.

## 2. Resumo do projeto

Um pequeno restaurante de hambúrgueres, que está crescendo, necessita uma
interface em que se possa realizar pedidos utilizando um _tablet_, e enviá-los
para a cozinha para que sejam preparados de forma ordenada e eficiente.

![burger-queen](https://user-images.githubusercontent.com/110297/42118136-996b4a52-7bc6-11e8-8a03-ada078754715.jpg)

Este projeto tem duas áreas: interface (cliente) e API (servidor). Nosso
cliente nos pediu para desenvolver uma interface que se integre com a API
que outra equipe de desenvolvedoras está trabalhando simultaneamente.

Desta vez temos um projeto 100% por demanda. Você sempre pode (e deve) fazer
sugestões de melhora e mudança, mas muitas vezes trabalhará em um projeto em que
primeiro deve se assegurar de cumprir os requisitos.

Estas são as informações que temos do cliente:

> Somos **Burger Queen**, um fast food 24hrs.
>
>A nossa proposta de serviço 24 horas foi muito bem recebida e, para continuar a
>crescer, precisamos de um sistema que nos ajude a receber pedidos de nossos
>clientes.
>
>Nós temos 2 menus. Um muito simples para o café da manhã:
>
>| Ítem                      |Preço R$|
>|---------------------------|------|
>| Café americano            |    5 |
>| Café com leite            |    7 |
>| Sanduíche de presunto e queijo|   10 |
>| Suco de fruta natural     |    7 |
>
>E outro menu para o resto do dia:
>
>| Ítem                      |Preço |
>|---------------------------|------|
>|**Hambúrgueres**           |   **R$**   |
>|Hambúrguer simples         |    10|
>|Hambúrguer duplo           |    15|
>|**Acompanhamentos**        |   **R$**   |
>|Batata frita               |     5|
>|Anéis de cebola            |     5|
>|**Bebidas**                |   **R$**   |
>|Água 500ml                 |     5|
>|Água 750ml                 |     7|
>|Bebida gaseificada 500ml   |     7|
>|Bebida gaseificada 750ml   |    10|
>
>Nossos clientes são bastante indecisos, por isso é muito comum que eles mudem o
>seu pedido várias vezes antes de finalizar.

A interface deve mostrar os dois menus (café da manhã e restante do dia), cada
um com todos os seus _produtos_. O usuário deve poder escolher que _produtos_
adicionar e a interface deve mostrar o _resumo do pedido_ com o custo total.

![out](https://user-images.githubusercontent.com/110297/45984241-b8b51c00-c025-11e8-8fa4-a390016bee9d.gif)

Além disso a cliente nos deu um
[link](https://app.swaggerhub.com/apis-docs/ssinuco/BurgerQueenAPI/2.0.0)
da documentação que especifica o comportamento esperado da API que
iremos expor por HTTP.
Lá podemos encontrar todos os detalhes dos _endpoints_, como por exemplo
que parâmetros esperam, o que devem responder, etc.

O objetivo principal é aprender a construir uma _interface web_ usando o
_framework_ escolhido (React ou Angular). Esses framework front-end ataca
o seguinte problema: **como manter a interface e estado sincronizados**.
Portanto, esta experiência espera familiarizá-la com o conceito de _estado da
tela_, e como cada mudança no estado vai refletir na interface (por exemplo,
toda vez que adicionamos um _produto_ para um _pedido_, a interface deve
atualizar a lista de pedidos e o total).

## 3. Objetivos de aprendizagem

Reflita e depois enumere os objetivos que quer alcançar e aplique no seu projeto. Pense nisso para decidir sua estratégia de trabalho.

### HTML

- [ ] **Uso de HTML semântico**

  <details><summary>Links</summary><p>

  * [HTML semântico](https://curriculum.laboratoria.la/pt/topics/html/html5/semantic-html)
  * [Semantics in HTML - MDN](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#Semantics_in_HTML)
</p></details>

### CSS

- [ ] **Uso de seletores de CSS**

  <details><summary>Links</summary><p>

  * [Intro a CSS](https://curriculum.laboratoria.la/pt/topics/css/css/intro-css)
  * [CSS Selectors - MDN](https://developer.mozilla.org/pt_BR/docs/Web/CSS/CSS_Selectors)
</p></details>

- [ ] **Modelo de caixa (box model): borda, margem, preenchimento**

  <details><summary>Links</summary><p>

  * [Modelo de Caixa e Display](https://curriculum.laboratoria.la/pt/topics/css/css/boxmodel-and-display)
  * [The box model - MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
  * [Introduction to the CSS box model - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
  * [CSS display - MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/display)
  * [display - CSS Tricks](https://css-tricks.com/almanac/properties/d/display/)
</p></details>

- [ ] **Uso de flexbox em CSS**

  <details><summary>Links</summary><p>

  * [A Complete Guide to Flexbox - CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
  * [Flexbox Froggy](https://flexboxfroggy.com/#pt-br)
  * [Flexbox - MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
</p></details>

- [ ] **Uso de CSS Grid Layout**

  <details><summary>Links</summary><p>

  * [A Complete Guide to Grid - CSS Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/)
  * [Grids - MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids)
</p></details>

- [ ] **Uso de media queries**

  <details><summary>Links</summary><p>

  * [CSS media queries - MDN](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Media_Queries/Using_media_queries)
</p></details>

### JavaScript

- [ ] **Uso de linter (ESLINT)**

- [ ] **Uso de identificadores descritivos (Nomenclatura e Semântica)**

#### Testing em Javascript

- [ ] **Testes unitários (unit tests)**

  <details><summary>Links</summary><p>

  * [Introdução ao Jest - Documentação oficial](https://jestjs.io/docs/pt-BR/getting-started)
</p></details>

- [ ] **Testes assíncronos**

  <details><summary>Links</summary><p>

  * [Testando Código Assíncrono - Documentação oficial](https://jestjs.io/docs/pt-BR/asynchronous)
</p></details>

- [ ] **Uso de mocks e espiões**

  <details><summary>Links</summary><p>

  * [Simulações Manuais - Documentação oficial](https://jestjs.io/docs/pt-BR/manual-mocks)
</p></details>

#### Módulos

- [ ] **Módulos de ECMAScript (ES modules)**

  <details><summary>Links</summary><p>

  * [import - MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/import)
  * [export - MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/export)
</p></details>

### Controle de Versões (Git e GitHub)

#### Git

- [ ] **Git: Instalação e configuração**

- [ ] **Git: Controle de versão com git (init, clone, add, commit, status, push, pull, remote)**

- [ ] **Git: Integração de mudanças entre ramos (branch, checkout, fetch, merge, reset, rebase, tag)**

#### GitHub

- [ ] **GitHub: Criação de contas e repositórios, configuração de chave SSH**

- [ ] **GitHub: Implantação com GitHub Pages**

  <details><summary>Links</summary><p>

  * [Site oficial do GitHub Pages](https://pages.github.com/)
</p></details>

- [ ] **GitHub: Colaboração pelo Github (branches | forks | pull requests | code review | tags)**

- [ ] **GitHub: Organização pelo Github (projects | issues | labels | milestones | releases)**

### HTTP

- [ ] **Consulta ou solicitação (request) e resposta (response).**

  <details><summary>Links</summary><p>

  * [Visão geral do protocolo HTTP - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Overview)
  * [Mensagens HTTP - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Messages)
</p></details>

- [ ] **Cabeçalhos (headers)**

  <details><summary>Links</summary><p>

  * [Cabeçalhos HTTP - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Headers)
</p></details>

- [ ] **Corpo (body)**

  <details><summary>Links</summary><p>

  * [Mensagens HTTP / Corpo - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Messages#corpo)
</p></details>

- [ ] **Verbos HTTP**

  <details><summary>Links</summary><p>

  * [Métodos de requisição HTTP - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Methods)
</p></details>

- [ ] **Códigos de status de HTTP**

  <details><summary>Links</summary><p>

  * [Códigos de status de respostas HTTP - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status)
  * [The Complete Guide to Status Codes for Meaningful ReST APIs - dev.to](https://dev.to/khaosdoctor/the-complete-guide-to-status-codes-for-meaningful-rest-apis-1-5c5)
</p></details>

- [ ] **Encodings e JSON**

  <details><summary>Links</summary><p>

  * [Introdução ao JSON - Documentação oficial](https://www.json.org/json-pt.html)
</p></details>

- [ ] **CORS (Cross-Origin Resource Sharing)**

  <details><summary>Links</summary><p>

  * [Cross-Origin Resource Sharing (CORS) - MDN](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/CORS)
</p></details>

### Angular

- [ ] **Components & templates**

  <details><summary>Links</summary><p>

  * [Angular Components Overview - Documentação oficial (em inglês)](https://angular.io/guide/component-overview)
  * [Introduction to components and templates - Documentação oficial (em inglês)](https://angular.io/guide/architecture-components#introduction-to-components)
</p></details>

- [ ] **Diretivas estruturais (ngIf / ngFor)**

  <details><summary>Links</summary><p>

  * [Writing structural directives - Documentação oficial (em inglês)](https://angular.io/guide/structural-directives)
</p></details>

- [ ] **@Input | @Output**

  <details><summary>Links</summary><p>

  * [Component interaction - Documentação oficial (em inglês)](https://angular.io/guide/component-interaction#component-interaction)
</p></details>

- [ ] **Criação e uso de serviços**

  <details><summary>Links</summary><p>

  * [Providing services - Documentação oficial (em inglês)](https://angular.io/guide/architecture-services#providing-services)
</p></details>

- [ ] **Gerenciamento de rotas**

  <details><summary>Links</summary><p>

  * [In-app navigation: routing to views - Documentação oficial (em inglês)](https://angular.io/guide/router)
</p></details>

- [ ] **Criação e uso de Observables**

  <details><summary>Links</summary><p>

  * [Observables in Angular - Documentação oficial (em inglês)](https://angular.io/guide/observables-in-angular)
</p></details>

- [ ] **Uso de HttpClient**

  <details><summary>Links</summary><p>

  * [Communicating with backend services using HTTP - Documentação oficial (em inglês)](https://angular.io/guide/http)
</p></details>

- [ ] **Estilos de componentes (ngStyle / ngClass)**

  <details><summary>Links</summary><p>

  * [Template syntax - Documentação oficial (em inglês)](https://angular.io/guide/template-syntax#built-in-directives)
</p></details>

### React

- [ ] **JSX**

  <details><summary>Links</summary><p>

  * [Introduzindo JSX - Documentação oficial](https://pt-br.react.dev/learn/writing-markup-with-jsx)
</p></details>

- [ ] **Componentes e propriedades (props)**

  <details><summary>Links</summary><p>

  * [Componentes e propriedades - Documentação oficial](https://pt-br.react.dev/learn/passing-props-to-a-component)
</p></details>

- [ ] **Manipulação de eventos**

  <details><summary>Links</summary><p>

  * [Manipulando eventos - Documentação oficial](https://pt-br.react.dev/learn/responding-to-events)
</p></details>

- [ ] **Listas e keys**

  <details><summary>Links</summary><p>

  * [Listas e chaves - Documentação oficial](https://pt-br.react.dev/learn/rendering-lists)
</p></details>

- [ ] **Renderização condicional**

  <details><summary>Links</summary><p>

  * [Renderização condicional - Documentação oficial](https://pt-br.react.dev/learn/conditional-rendering)
</p></details>

- [ ] **Elevação de estado**

  <details><summary>Links</summary><p>

  * [Elevação de estado - Documentação oficial](https://pt-br.react.dev/learn/sharing-state-between-components)
</p></details>

- [ ] **Hooks**

  <details><summary>Links</summary><p>

  * [Introduzindo Hooks - Documentação oficial](https://pt-br.react.dev/reference/react)
</p></details>

- [ ] **CSS modules**

  <details><summary>Links</summary><p>

  * [Adding a CSS Modules Stylesheet - Documentação de Create React App (em inglês)](https://vitejs.dev/guide/features.html#css-modules)
</p></details>

- [ ] **React Router**

  <details><summary>Links</summary><p>

  * [Quick Start - Documentação oficial (em inglês)](https://reactrouter.com/en/main/start/tutorial)
</p></details>

### Vue

- [ ] **Instância de Vue.js**

  <details><summary>Links</summary><p>

  * [A Instância Vue - Documentação oficial](https://br.vuejs.org/v2/guide/instance.html)
</p></details>

- [ ] **Dados e métodos**

  <details><summary>Links</summary><p>

  * [Dados e métodos - Documentação oficial](https://br.vuejs.org/v2/guide/instance.html#Dados-e-Metodos)
</p></details>

- [ ] **Uso e criação de componentes**

  <details><summary>Links</summary><p>

  * [Conceitos Básicos de Componentes - Documentação oficial](https://br.vuejs.org/v2/guide/components.html)
</p></details>

- [ ] **Props**

  <details><summary>Links</summary><p>

  * [Passando dados aos componentes filhos com Props - Documentação oficial](https://br.vuejs.org/v2/guide/components.html#Passando-Dados-aos-Filhos-com-Props)
</p></details>

- [ ] **Diretivas (v-bind | v-model)**

  <details><summary>Links</summary><p>

  * [v-bind - Documentação oficial](https://br.vuejs.org/v2/api/#v-bind)
  * [Binding/Interligações em Formulários - Documentação oficial](https://br.vuejs.org/v2/guide/forms.html)
</p></details>

- [ ] **Iteração (v-for)**

  <details><summary>Links</summary><p>

  * [Array em elementos com v-for - Documentação oficial](https://br.vuejs.org/v2/guide/list.html#Array-em-Elementos-com-v-for)
</p></details>

- [ ] **Eventos (v-on)**

  <details><summary>Links</summary><p>

  * [Manipulação de eventos - Documentação oficial](https://br.vuejs.org/v2/guide/events.html)
</p></details>

- [ ] **Dados Computados e Observadores**

  <details><summary>Links</summary><p>

  * [Dados Computados e Observadores](https://br.vuejs.org/v2/guide/computed.html)
</p></details>

- [ ] **Routing**

  <details><summary>Links</summary><p>

  * [Getting Started - Documentação oficial de Vue Router](https://router.vuejs.org/guide/#html)
</p></details>

- [ ] **Classes e Estilos**

  <details><summary>Links</summary><p>

  * [Interligações de Classe e Estilo - Documentação oficial](https://br.vuejs.org/v2/guide/class-and-style.html)
</p></details>

### Typescript

- [ ] **Narrowing**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/narrowing.html)
</p></details>

- [ ] **Decoradores**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/decorators.html)
</p></details>

#### Tipos básicos

- [ ] **Verificação estática de tipos**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/basic-types.html#static-type-checking)
</p></details>

- [ ] **Rigor**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript 1](https://www.typescriptlang.org/docs/handbook/2/basic-types.html#strictness)
  * [Documentação oficial do Typescript 2](https://www.typescriptlang.org/tsconfig#Type_Checking_6248)
</p></details>

- [ ] **Tipos primitivos**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#the-primitives-string-number-and-boolean)
</p></details>

- [ ] **Arrays**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#arrays)
</p></details>

- [ ] **Tipo `any`**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#any)
</p></details>

- [ ] **Funções**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#functions)
  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/functions.html)
</p></details>

- [ ] **Tipos de união**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#union-types)
</p></details>

- [ ] **Alias de tipos**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-aliases)
</p></details>

- [ ] **Interfaces**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#interfaces)
</p></details>

- [ ] **Type assertions**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#type-assertions)
</p></details>

- [ ] **Tipos literais**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#literal-types)
</p></details>

- [ ] **null e undefined**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#null-and-undefined)
</p></details>

- [ ] **Enums**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#enums)
</p></details>

##### Tipos Objecto _(Tipos básicos)_

- [ ] **Propriedades opcionais**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html#optional-properties)
</p></details>

#### Classes

- [ ] **Visibilidade dos membros da classe (public, private, protected)**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#member-visibility)
</p></details>

- [ ] **Membros estáticos da classe**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#static-members)
</p></details>

- [ ] **this**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#this-at-runtime-in-classes)
</p></details>

- [ ] **Classes abstratas**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#abstract-classes-and-members)
</p></details>

##### Membros da classe _(Classes)_

- [ ] **Campos**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#fields)
</p></details>

- [ ] **Constructors**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.htmll#constructors)
</p></details>

- [ ] **Métodos**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#methods)
</p></details>

- [ ] **Getters e Setters**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#getters--setters)
</p></details>

##### Herança de classe _(Classes)_

- [ ] **implements Cláusulas**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#implements-clauses)
</p></details>

- [ ] **extends Cláusulas**

  <details><summary>Links</summary><p>

  * [Documentação oficial do Typescript](https://www.typescriptlang.org/docs/handbook/2/classes.html#extends-clauses)
</p></details>

### Centrado no usuário

- [ ] **Desenhar e desenvolver um produto ou serviço colocando as usuárias no centro**

### Design de produto

- [ ] **Criar protótipos para obter feedback e iterar**

- [ ] **Aplicar os princípios de desenho visual (contraste, alinhamento, hierarquia)**

### Pesquisa

- [ ] **Planejar e executar testes de usabilidade**

## 4. Considerações gerais

Este projeto deve ser implementado em duplas e, para trabalhar com o backend,
sugerimos que você escolha um dos seguintes métodos:

1. Usando uma mock API. Você pode criar sua própria mock API com as ferramentas
  [json-server](https://www.npmjs.com/package/json-server) e
  [json-server-auth](https://www.npmjs.com/package/json-server-auth), ou pode
  fazer um fork e clonar
  [este repositório de uma mock API](https://github.com/Laboratoria/burger-queen-api-mock)
  que desenvolvemos. Esta mock API deve se comportar conforme definido
  [na documentação.](https://app.swaggerhub.com/apis-docs/ssinuco/BurgerQueenAPI/2.0.0)

2. Consumindo uma API implantada. Você pode usar uma API que suas colegas
  desenvolverão em seu projeto Burger Queen API, ou pode implantar sua mock API.
  Aqui está [um exemplo de como implantar sua mock com o Vercel.](https://medium.com/@phillipnzaujunior/unleashing-the-power-of-mock-apis-deploying-your-fake-rest-api-to-vercel-d1cbd95b4452)

Você pode começar usando uma mock API e, a qualquer momento do projeto, migrar
para a API implantada. Isso costuma ocorrer no Desenvolvimento Web,
quando é necessário avançar com a implementação do frontend enquanto
as pessoas responsáveis pelo backend ainda estão desenvolvendo a API.

O intervalo de tempo estimado para concluir o projeto é de 3 a 5 Sprints.

Trabalhe integralmente uma história de usuário antes de passar para a próxima.
Cumpra todas as histórias possíveis dentro do tempo especificado.

A lógica do projeto deve ser totalmente implementada em JavaScript (ES6 +), HTML
e CSS e empacotada de forma automatizada.

Um dos principais objetivos deste projeto é aprender a usar uma biblioteca ou
framework popular para desenvolver uma aplicação web. Você deve escolher entre
[React](https://pt-br.react.dev/) ou [Angular](https://angular.io/).

Tenha em mente que se você escolher o Angular, é obrigatório usar [TypeScript](https://www.typescriptlang.org/).
O _TypeScript_ é uma linguagem de programação fortemente tipada baseada
em JavaScript.

Se você optar pelo React, a decisão de usar o TypeScript é opcional (mas
recomendamos!). Aqui você pode encontrar mais informações sobre
como iniciar seu projeto com [Typescript e React](https://pt.vitejs.dev/guide/#scaffolding-your-first-vite-project).

Se você usa Angular, **recomendamos usar a versão 14**. Para isso, é necessário ter instalada a versão 12 do NodeJS. 
Você pode encontrar um guia de instalação 
[aqui](https://github.com/Laboratoria/frontend-technologies-simple-example/tree/main/angular-example)
ou consultar com seus coaches.

O aplicativo deve ser um _Single Page App_. Os pedidos serão enviados por meio
de um _tablet_, mas **não queremos um aplicativo nativo**, mas sim um aplicativo
Web que seja **mobile-first**.

Precisamos pensar bem sobre o UX para aqueles que vão receber os pedidos, o
tamanho e a aparência dos botões, a visibilidade do estado atual do pedido, etc.

A aplicação deve seguir 80% ou mais das pontuações de Performance, Progressive
Web App, Accessibility e Best Practices do Lighthouse.

O aplicativo deve fazer uso de `npm-scripts` e ter scripts `start`, `test`,
`build` e `deploy`, que são responsáveis por inicializar, rodar os testes,
empacotar e fazer deploy do aplicativo, respectivamente.

Os testes unitários devem cobrir um mínimo de 90% de _statements_, _functions_,
_lines_ e _branches_.

Por outro lado, vocês devem definir a estrutura das pastas e arquivos que considerem
necessários. Você pode estruturá-los de acordo com as convenções do _framework_ escolhido.
Portanto, os _testes_ e os _setups_ necessários para executá-los
serão feitos por você.

## 5. Critérios mínimos de aceitação do projeto

### Definição do produto

O [_Product Owner_](https://www.youtube.com/watch?v=7lhnYbmovb4) nos apresentou
este _backlog_ que é o resultado do seu trabalho com o cliente até hoje.

***

#### [Historia de usuario 1] Garçom/Garçonete deve poder entrar no sistema, caso o admin já lhe tenha dado as credenciais

Eu, como garçom/garçonete quero entrar no sistema de pedidos.

##### Critérios de aceitação

O que deve acontecer para satisfazer as necessidades do usuário?

* Acessar uma tela de login.
* Inserir email e senha.
* Receber mensagens de erros compreensíveis, conforme o erro e as informações inseridas.
* Entrar no sistema de pedidos caso as credenciais forem corretas.

##### Definição de pronto

O acordado abaixo deve acontecer para dizer que a história está terminada:

* Você deve ter recebido _code review_ de pelo menos uma parceira.
* Fez _testes_ unitários e, além disso, testou seu produto manualmente.
* Você fez _testes_ de usabilidade e incorporou o _feedback_ do usuário.
* Você deu deploy de seu aplicativo e marcou sua versão (tag git).

***

#### [História de usuário 2] Garçom/Garçonete deve ser capaz de anotar o pedido do cliente

Eu como garçom/garçonete quero poder anotar o pedido de um cliente para não
depender da minha memória, saber quanto cobrar e poder enviar os pedidos para a
cozinha para serem preparados em ordem.

##### Critérios de aceitação

O que deve acontecer para satisfazer as necessidades do usuário?

* Anotar o nome do cliente.
* Adicionar produtos aos pedidos.
* Excluir produtos.
* Ver resumo e o total da compra.
* Enviar o pedido para a cozinha (guardar em algum banco de dados).
* Funcionar bem em um _tablet_.

##### Definição de pronto

O acordado abaixo deve acontecer para dizer que a história está terminada:

* Você deve ter recebido _code review_ de pelo menos uma parceira.
* Fez _testes_ unitários e, além disso, testou seu produto manualmente.
* Você fez _testes_ de usabilidade e incorporou o _feedback_ do usuário.
* Você deu deploy de seu aplicativo e marcou sua versão (tag git).

***

#### [História de usuário 3] Chefe de cozinha deve ver os pedidos

Eu como chefe de cozinha quero ver os pedidos dos clientes em ordem, poder
marcar que estão prontos e poder notificar os garçons/garçonetes que o pedido
está pronto para ser entregue ao cliente.

##### Critérios de aceitação

* Ver os pedidos ordenados à medida em que são feitos.
* Marcar os pedidos que foram preparados e estão prontos para serem servidos.
* Ver o tempo que levou para preparar o pedido desde que chegou, até ser marcado
  como concluído.

##### Definição de pronto

* Você deve ter recebido _code review_ de pelo menos uma parceira.
* Fez _testes_ unitários e, além disso, testou seu produto manualmente.
* Você fez _testes_ de usabilidade e incorporou o _feedback_ do usuário.
* Você deu deploy de seu aplicativo e marcou sua versão (tag git).

***

#### [Historia de usuário 4] Garçom/Garçonete deve ver os pedidos prontos para servir

Eu como garçom/garçonete quero ver os pedidos que estão prontos para entregá-los
rapidamente aos clientes.

##### Critérios de aceitação

* Ver a lista de pedidos prontos para servir.
* Marcar os pedidos que foram entregues.

##### Definição de pronto

* Você deve ter recebido _code review_ de pelo menos uma parceira.
* Fez _testes_ unitários e, além disso, testou seu produto manualmente.
* Você fez _testes_ de usabilidade e incorporou o _feedback_ do usuário.
* Você deu deploy de seu aplicativo e marcou sua versão (tag git).
* Os dados devem ser mantidos intactos, mesmo depois que um pedido for
  finalizado. Tudo isso para poder ter estatísticas no futuro.

## 6. Implantação

Você pode escolher o provedor (ou provedores) que preferir junto
com o mecanismo de implantação e a estratégia de hospedagem.
Lembre-se de que, se você mock da API, você também tem que implantá-la.
Te recomendamos explorar as seguintes opcões:

* [Vercel](https://vercel.com/) é uma plataforma que nos permite implantar
nossa aplicação web estática (HTML, CSS e JavaScript) e também nos permite
implantar aplicações web rodando no servidor (Node.js).
* [Netlify](https://www.netlify.com/) como Vercel, é uma plataforma
que nos permite implantar nossa aplicação web estática (HTML, CSS e
JavaScript) e também nos permite implantar aplicações web rodando
no servidor (Node.js).

## 7. Pistas, tips e leituras complementares

Participe do canal do Slack
[#project-bq-api-client](https://claseslaboratoria.slack.com/archives/C04A0GS1WJX)
para conversar e pedir ajuda no projeto.

### Frameworks / bibliotecas

* [React](https://react.dev/)
* [Angular](https://angular.io/)

### Ferramentas

* [npm-scripts](https://docs.npmjs.com/misc/scripts)
* [Babel](https://babeljs.io/)
* [webpack](https://webpack.js.org/)
* [json-server](https://www.npmjs.com/package/json-server)

### PWA

* [Seu primeiro Progressive Web App - Google developers](https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/?hl=es)
* [Progressive Web Apps - codigofacilito.com](https://codigofacilito.com/articulos/progressive-apps)
* [Usando Service Workers - MDN](https://developer.mozilla.org/pt-BR/docs/Web/API/Service_Worker_API/Using_Service_Workers)

## 8. Funcionalidades opcionais

Se você tiver concluído todas as funcionalidades do projeto,
nós o convidamos a trabalhar nas seguintes histórias de usuário:

***

### [Historia de usuário 5] Administrador(a) de loja deve administrar seus funcionários

Eu como administrador(a) de loja quero gerenciar os usuários da
plataforma para manter atualizado as informações de meus funcionários.

#### Critérios de aceitação

* Ver lista de funcionários.
* Adicionar funcionários.
* Excluir funcionários.
* Atualizar dados dos funcionários.

#### Definição de pronto

* Você deve ter recebido _code review_ de pelo menos uma parceira.
* Fez _testes_ unitários e, além disso, testou seu produto manualmente.
* Você fez _testes_ de usabilidade e incorporou o _feedback_ do usuário.
* Você deu deploy de seu aplicativo e marcou sua versão (tag git).

***

### [História de usuário 6] Administrador(a) de loja deve administrar os produtos

Eu como administrador(a) de loja quero gerenciar os produtos
para manter atualizado o menu.

#### Critérios de aceitação

* Ver lista de produtos.
* Adicionar produtos.
* Excluir produtos.
* Atualizar dados de produtos.

#### Definição de pronto

* Você deve ter recebido _code review_ de pelo menos uma parceira.
* Fez _testes_ unitários e, além disso, testou seu produto manualmente.
* Você fez _testes_ de usabilidade e incorporou o _feedback_ do usuário.
* Você deu deploy de seu aplicativo e marcou sua versão (tag git).
