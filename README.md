![](/mobile/src/assets/logo@2x.png)</br></br>

## Este projeto foi desenvolvido durante a *Next Level Week #01* da *Rocketseat* com o objetivo de ajudar as pessoas a fazerem o descarte correto de resíduos.

### Funcionalidades

- [x] Cadastro de estabelecimentos com integração de mapas (via *web*)
- [x] Visualização dos estabelecimentos cadastrados com filtragem por resíduos (via *mobile*)
- [x] Interação com estabelecimentos via *whatsapp* ou *email* na versão *mobile*

### Tecnologias utilizadas

* Na versão *web* utilizamos [ReactJs](https://reactjs.org/) juntamente com [TypeScript](https://www.typescriptlang.org/).
* A versão *mobile* foi desenvolvida utilizando [ReactNative](https://reactnative.dev/) e [TypeScript](https://www.typescriptlang.org/).
* No *back-end* foi utilizado [NodeJs](https://nodejs.org/en/) e [TypeScript](https://www.typescriptlang.org/).
* Para o banco de dados foi utilizado o [KnexJs](http://knexjs.org/) como interpretador de comandos *SQL* junto com o *SQLite3*.
* Para o *deploy* da aplicação na versão *mobile* foi utilizado o [Expo](https://expo.io/).

### Instalando as dependências
Para instalar as dependências, basta executar um dos seguintes comandos dentro das pastas *server*, *web* e *mobile*:
```bash
npm install
# ou com yarn
yarn
```

## Configurando o servidor
Antes de testar a aplicação, é primordial que você configure o seu ambiente para o funcionamento correto do projeto.<br/>

Execute o seguinte comando na pasta *server*:
```bash
npm run knex:migrate
# ou com yarn
yarn knex:migrate
```
Este comando irá criar os esquemas (tabelas): *points*, *items* e *point_items*.
Você pode consultar as estruturas das tabelas a serem criadas [aqui](/server/src/database/migrations).

### Definindo itens do app

Agora precisamos definir os itens que serão disponibilizados no *app*. 
Obs: estes itens são chamado posteriormente durante o cadastro de um estabelecimento e também durante a visualização dos 
pontos de coleta na versão *mobile*.

```bash
npm run knex:seed
# ou com yarn
yarn knex:seed
```
Você pode seguir este tutorial para visualizar os dados diretamente pelo [VsCode](https://github.com/AlexCovizzi/vscode-sqlite).

### Executando o servidor
Entre na pasta *server* e execute o seguinte comando:
```bash
npm run dev
# ou com yarn
yarn dev
```

Após todas as etapas, seu servidor deverá estar funcionando sem nenhum problema.

## Rodando a versão *Web*
Para rodar essa versão, basta entrar na pata *web* e executar o seguinte comando:
```bash
npm run start
# ou com yarn
yarn start
```

### Cadastrando um estabelecimento
Segue uma prévia do cadastro de um estabelecimento com *upload* de imagem e integração com mapas.

![Point Register](https://i.makeagif.com/media/6-07-2020/4dXevP.gif)
