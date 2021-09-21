# Desenvolvimento de aplicações para internet com ReactJS
## Requisitos
- Node.js 
- React
- IDE

## Após clonar o projeto execute
Instalar as dependências:
>npm install

React Scripts:
>npm install react-scripts --save

Yarn Start:
>yarn start

## Stateful
Possui gerenciamento de estados no componente. Construídos usando classes em JS.

## Stateless 
Não possui gerenciamento de estados no componente. Construídos usando funções em JS.

## Stateful vs Stateless 
A nomenclatura foi atualizada.
- Class Components
- Function Components
Com hooks, estados são manipuláveis em function components

## Componente controlado
- Tanto select, input ou textarea aceitam um atributo value
- Podemos mudar esse valor usando o atributo onChange

## Componente não controlado
A tag input é read-only

## Bibliotecas de formulários
- Formik
- Redux-forms

## Ciclo de vida
![ciclodevida](https://user-images.githubusercontent.com/72028645/134172165-a434f09c-282c-4b5b-b3d6-052680a6f05f.png)

## Arquitetura Flux
Flux é um padrão de projeto para tráfego de dados de maneira unidirecional

### Action
É como um telégrafo, ele formata a mensagem a ser enviada

### Dispatcher 
É como um telefonista, ele sabe todos os callbacks para diferentes Stores

### Store
É como um gerente super controlador, ele guarda as informações e todas as alterações tem que ser feitas por ele mesmo, mais ninguém

### View
É como um gerente intermediário (middleware) que recebe as notificações da store e passa os dados para as visões abaixo dela

## Diversas implementações
- Redux (mais popular)
- Reflux
- Mobx
- Vuex (baseado em Redux e Elm)
- NgRx/store (baseado em Redux e RxJS)

## Bibliotecas baseadas em Flux
- Servem para comunicação entre componentes
- Centralizam a informação
- "Flux libraries are like glasses: you'll know when you need them" - Dan Abramov

## Redux
3 princípios:
- Single source of truth: Uma única store (diferente de Flux, que tem várias stores e o dispatcher conecta as stores
- State é read-only
- Mudanças são feitas com pure functions (o estado é imutável)

### Actions
- Actions são como o Flux
- Diferença: Actions não enviam a action em si para o dispatcher
- Retornam um objeto de action formatado

### Store
- Em Flux: diversas Stores
- Em Redux: uma única Store
- A Store cuida de toda a árvore de estados
- Os reducers descobrem qual estado muda

### Reducers
- Em Redux não há dispatcher (simplifica e divide o trabalho da Store)
- A Store se conecta ao root reducer, que divide os estados em pequenos reducers para descobrir como lidar com esse estado
- Os estados são imutáveis

### Views
Em React, adiciona na camada de View 3 novos conceitos para conectar a View à Store:
1. Provider
2. connect()
3. selector

## Instalando o Redux
React Redux:
>npm install react-redux
>npm install --save-dev redux-devtools

Instale a extensão:
![redux](https://user-images.githubusercontent.com/72028645/134182530-f3f88b98-5755-4c8f-aa83-0db3f28ec9b4.png)

- Abra a extensão pelo inspetor do navegador

## APIs HTTP
- Servem para conectar um ou mais servidores HTTP
- GET, POST, DELETE, PUT
- Fetch API
- Axios

### Fetch API
- Nativa do browser
- Oferece uma alternativa ao XMLHttpRequest() e jQuery.ajax()
- Suporte a Service Workers
- Não envia e nem recebe cookies (precisa definir a opção credentials)
- Não rejeita o status do erro HTTP

### Axios
- Lib de HTTP API
- Cross-browser
- Pode monitorar o progresso de um request
- Melhor treinamento de erros
- Melhor teste
- Para instalar:
>yarn add axios

## Entendendo o código
`\src\aula-1\parte-1\componentes\ClassName.jsx`: Estilização ClassName <br>
`\src\aula-1\parte-1\componentes\Inline.jsx`: Estilização Inline <br>
`\src\aula-1\parte-1\componentes\Styled.jsx`: Estilização Styled <br>
`\src\aula-1\parte-2\TodoListStatefull.jsx`: Stateful <br>
`\src\aula-1\parte-2\TodoListStateless.jsx`: Stateless <br>
`\src\aula-1\parte-2\TodoListFunctional.jsx`: Hook <br>
`\src\aula-1\parte-3\components\NameForm.jsx`: Componente controlado <br>
`\src\aula-1\parte-3\components\SorveteForm.jsx`: Componente controlado <br>
`\src\aula-1\parte-3\components\FileInput.jsx`: Componente não controlado <br>
`\src\aula-2\components\Counter.jsx`: Redux <br>
`\src\aula-3\Components\Topico3`: Axios <br> 
`\src\redux`: Redux <br>

## Documentações
- [Estilização de componentes e elementos CSS](https://www.w3schools.com/react/react_css.asp)
- [Stateful e Stateless](https://programmingwithmosh.com/javascript/stateful-stateless-components-react/)
