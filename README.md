# nodets-canil
Projeto feito em Node JS + Typescript

### Pré-requisitos globais:
`npm install -g nodemon typescript ts-node`

### Configurando
`npm init` iniciando o projeto
`tsc --init` configuração Typescript
Abrir o arquivo do tsconfig.json e modificar para:
`"outDir": ./dist`,
`"rootDir": ./src`,
Desmarcar o comentário
`"moduleResolution": "node"`,

### Instalação
`npm install express mustache-express dotenv`

`npm install --save-dev @types/express @types/mustache-express @types/node`

Dentro do arquivo package.json
 "Scripts": {
     "start-dev": "nodemon -e ts,json,mustache src/server.ts"
 },

### Para rodar o projeto
`npm run start-dev`

### Atualizando o projeto no repositório
`git --global config user.teuNome`
`git --global config user.teuEmail`

`git add .`
`git commit -m "nome do teu commit"`
`git push` Vai enviar arquivos novos para o repositório

### Configurando o Projeto para Javascript
 -> Mudar no package.json
 -> Adicionar a linha 
  "engines": {
    "node": "14.x" colocar a versão do node
  },

  -> Criar um arquivo: Procfile
  -> Adiciona a linha no arquivo: web: npm start

  -> `npm install --save-dev copyfiles` instalação de biblioteca
  -> No arquivo package.json adicionar no Scripts:
  -> "start": "node dist/server.js",
  -> "postinstall": "tsc && copyfiles -u 1 src/**/*.mustache dist/",

  -> Rodar o código no terminal:
  -> `npm run postinstall`

  ### Heroku
  -> Colocar o projeto na web
  -> Instalar o Heroku no PC.
  -> No terminal digitar: 
  -> heroku login
  -> heroku create
  -> `npm install typescript`
  -> No arquivo package.json colococar no scripts:
  -> "tsc": "tsc",
  -> Adicionar no início da linha "postinstall": "npm run tsc ..."

  ### Atualizar o repositório
  -> `git add .`
  -> `git commit -m "heroku setup - add tsc"`
  -> `git push heroku main`

  ### Abrir o link criado do projeto no Heroku
  -> heroku open
