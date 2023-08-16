<div align="center">
	 <img alt="JSON" align="center" src="./public/potato-pay.png" width="140px">
</div>

# PotatoPay
Temos 2 tipos de usuários, os comuns e lojistas, ambos têm carteira com dinheiro e realizam transferências entre eles.

## Objetivo: PotatoPay Simplificado

Temos 2 tipos de usuários, os comuns e lojistas, ambos têm carteira com dinheiro e realizam transferências entre eles. Vamos nos atentar **somente** ao fluxo de transferência entre dois usuários.

Requisitos:

- Para ambos tipos de usuário, precisamos do Nome Completo, CPF, e-mail e Senha. CPF/CNPJ e e-mails devem ser únicos no sistema. Sendo assim, seu sistema deve permitir apenas um cadastro com o mesmo CPF ou endereço de e-mail.

- Usuários podem enviar dinheiro (efetuar transferência) para lojistas e entre usuários. 

- Lojistas **só recebem** transferências, não enviam dinheiro para ninguém.

- Validar se o usuário tem saldo antes da transferência.

- Antes de finalizar a transferência, deve-se consultar um serviço autorizador externo, use este mock para simular (https://run.mocky.io/v3/8fafdd68-a090-496f-8c9a-3442cf30dae6).

- A operação de transferência deve ser uma transação (ou seja, revertida em qualquer caso de inconsistência) e o dinheiro deve voltar para a carteira do usuário que envia. 

- No recebimento de pagamento, o usuário ou lojista precisa receber notificação (envio de email, sms) enviada por um serviço de terceiro e eventualmente este serviço pode estar indisponível/instável. Use este mock para simular o envio (http://o4d9z.mocklab.io/notify). 

- Este serviço deve ser RESTFul.

### Detalhes do projeto

## 🚀 Tecnologias utilizadas

- [Typescript](https://www.typescriptlang.org)
- [Nodejs](https://nodejs.org/en/ 'Nodejs')
- [Nestjs](https://nestjs.com/ 'Nestjs')
## 💻 Iniciando o projeto localmente

### Requerimentos

- [Node.js](https://nodejs.org/en/)
- [NPM](https://www.npmjs.com/)

**Clone o projeto e acesse a pasta do repositório**

```bash
# git clone REPOSITÓRIO_PROJETO && cd/NOME_PROJETO
$ git clone https://github.com/Gabriel-souzaa/potato-pay.git && cd potato-pay
```

**Siga os passos**

```bash
# Instale as dependências
$ npm i

# Realize os testes para verificar se está tudo OK.
$ npm run test

# Rodar as migrações do prisma e gerar o database
$ npx prisma migrate dev
$ npx prisma generate

# inicie o projeto como dev
$ npm run start:dev

# Se todos os passos foram seguidos corretamente a api deve ser iniciada
```