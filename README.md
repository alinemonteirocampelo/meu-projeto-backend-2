# meu-projeto-backend-2

# Meu Projeto Backend 🚀

Este projeto apresenta a configuração inicial de um **backend utilizando Node.js, TypeScript e Express**. O objetivo é criar um servidor HTTP simples que ficará disponível na porta **8081**.

## Tecnologias utilizadas 📋

* Node.js
* TypeScript
* Express
* tsx
* npm

## Preparando o ambiente ⚙️

Inicialmente, crie uma pasta para o projeto e acesse-a pelo terminal.

Execute os seguintes comandos para configurar o TypeScript:

```bash
npm init -y
npm i -D typescript @types/node tsx
npx tsc --init
```

Em seguida, instale o framework Express e seus tipos para TypeScript:

```bash
npm install express
npm install -D @types/express
```

## Estrutura do projeto 📁

Após a configuração, a estrutura do projeto ficará semelhante a esta:

```text
meu-projeto-backend
│
├── node_modules
├── src
│   └── app.ts
├── package.json
└── tsconfig.json
```

A pasta `src` será utilizada para armazenar os arquivos do código-fonte. O arquivo `app.ts` será responsável pela criação e inicialização do servidor.

## Criando o servidor com Express 🖥️

Dentro da pasta `src`, crie o arquivo:

```text
src/app.ts
```

Adicione o seguinte código:

```typescript
// Importa a biblioteca Express e também o tipo Express
// O Express será utilizado para criar o servidor web
import express from "express";
import type { Express } from "express";

// Cria uma aplicação Express
// A função express() devolve um objeto que representa o servidor da aplicação
const app: Express = express();

// Define a porta onde o servidor ficará disponível
// Neste caso, o servidor poderá ser acessado pela porta 8081
const PORT: number = 8081;

// Inicializa o servidor utilizando a porta definida
// O método listen() faz o servidor começar a "escutar" requisições HTTP
app.listen(PORT, () => {
  console.log(`Servidor rodando em http://localhost:${PORT}`);
});
```

### Entendendo o código 🔎

* `express()` cria a aplicação do servidor.
* `PORT` define a porta utilizada pelo servidor.
* `app.listen()` inicia o servidor.
* `console.log()` exibe uma mensagem informando que o servidor foi iniciado.

## Configurando o script de execução 📦 

Abra o arquivo `package.json` e altere a seção `"scripts"` para:

```json
"scripts": {
  "dev": "tsx watch src/app.ts"
}
```

O comando `tsx watch` permite executar o arquivo TypeScript e reiniciar automaticamente o servidor sempre que houver alterações no código.

## Executando o servidor 📦 

Para iniciar o servidor, execute no terminal:

```bash
npm run dev
```

Se tudo estiver configurado corretamente, será exibida a mensagem:

```text
Servidor rodando em http://localhost:8081
```

O servidor poderá então ser acessado pelo navegador através do endereço:

```text
http://localhost:8081
```

## Resultado esperado ✅

Ao executar o projeto, o Express ficará responsável por iniciar um servidor local na porta **8081**.

Este projeto representa a configuração inicial de um backend e poderá posteriormente receber **rotas, APIs, requisições HTTP, conexão com banco de dados e outras funcionalidades**.

## Objetivo do projeto 📚

O objetivo desta atividade é aprender a:

* Configurar um projeto Node.js com TypeScript;
* Instalar e configurar o Express;
* Criar um servidor HTTP;
* Organizar a estrutura de um projeto backend;
* Executar um servidor utilizando `tsx`;
* Compreender a inicialização de uma aplicação Express.
