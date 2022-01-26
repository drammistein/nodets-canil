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