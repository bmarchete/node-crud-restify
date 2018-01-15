# Aplicação RESTful com Node.js

Este repositório contem a aplicação RESTful desenvolvida com Node.js que controla as operações CRUD em um banco de dados MySQL. Você pode encontrar um vídeo-cast com a explicação do desenvolvimento acessando o link https://youtu.be/Hel9igamKF0

Os seguintes módulos e ferramentas foram utilizados para o desenvolvimento da aplicação:

Cliente de acesso ao servidor: https://www.getpostman.com/

Módulo para manter o servidor funcionando: https://github.com/remy/nodemon

Framework para rotas REST: https://github.com/restify/node-restify

Plugin para definir mensagens de erro: https://github.com/restify/errors

Módulo ORM para Mysql: https://github.com/tgriesser/knex, http://knexjs.org

## Instalação e execução

Para testar a aplicação, você deve ter o MySQL instalado, com um banco de dados e uma tabela já criados.
No arquivo index.js, troque os valores de configuração do MySQL por aqueles utilizados por você.

```javascript
var knex = require('knex')({
  client: 'mysql',
  connection: {
    host : 'seu_host',
    user : 'seu_usuario',
    password : 'sua_senha',
    database : 'seu_banco'
    }
});
```

Acesse o terminal e execute o comando `npm i -g nodemon` para instalar o nodemon como global.

Em seguida, dentro da pasta do projeto, execute

```
npm install
```

Após concluída a instalação, execute o comando `nodemon index.js`

A partir do **Postman**, basta acessar as rotas criadas com os verbos http corretos.
