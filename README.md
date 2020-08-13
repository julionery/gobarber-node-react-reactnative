<h3 align="center">
    <img alt="Logo" title="#logo" width="250px" src="https://raw.githubusercontent.com/julionery/docs/12512ed22b35576b0e8e5b8d409f89fa3a50b7d8/GoBarber/logo.svg">
</h3>

## :page_with_curl: Sobre:

Este repositório contém um API REST em Node.js como back-end, uma aplicação em ReactJS como front-end e um app mobile em React Native, todos utilizando TypeScript.

GoBarber é uma plataforma de agendamento de serviços para proprietários de barbearias ou salões de beleza. Nessa aplicação o usuário consegue ter acesso a todos os prostadores de serviços cadastrados através de um aplicativo mobile, com isso usuário consegue escolher um prestador para marcar seu agendamento.

Já o prestador de serviço, através de um interface Web, consegue ter acesso a todos os seus horários, podendo ver todos os que estão ocupados quanto os que estão disponíveis.

[SERVER](https://github.com/julionery/gobarber-node-react-reactnative/tree/master/server) - Node.js: é uma API REST que faz todo o CRUD da aplicação, persistência de dados, tratativa de exceções e que serve dados tanto ao front-end quanto ao mobile.

[WEB](https://github.com/julionery/gobarber-node-react-reactnative/tree/master/web) - ReactJS: é uma página Web no qual o prestador de serviço tem acesso a todo o seu calendário de agendamentos.

[MOBILE](https://github.com/julionery/gobarber-node-react-reactnative/tree/master/mobile) - React Native: é um aplicativo em que o usuário tem acesso a todos os prestadores de serviço cadastrados no App, com isso ele pode fazer um agendamento que o prestador de preferência.

<h3 align="center">
    <img alt="Web" title="Web" src="https://github.com/julionery/docs/blob/master/GoBarber/gobarber-signup.gif?raw=true">
</h3>  

<h3 align="center">
    <img alt="Mobile" title="Mobile" width="300px" src="https://github.com/julionery/docs/blob/master/GoBarber/gobarber-signup-mobile.gif?raw=true?">
</h3>  

## Funcionalidades:
- **RF** - Requisitos Funcionais
- **RNF** - Requisitos Não Funcionais
- **RN** - Regras de Negócio

- [x] Cadastro de usuário;
  - [x] **RF** - O usuário deve poder cadastrar o seu nome, e-mail e senha;
  - [x] **RN** - O cadastro de usuário não deve permitir dois usuários com o mesmo e-mail;
  - [x] **RN** - A senha do usuário deve ser criptografada;
- [x] Login;
  - [x] **RF** - O usuário deve poder realizar o login;
  - [x] **RN** - O usuário não pode acessar o sistema com um e-mail não cadastrado;
  - [x] **RN** - O usuário não pode acessar o sistema com uma senha inválida;
- [x] Recuperação de senha;
  - [x] **RF** - O usuário deve poder recuperar sua senha informando o seu e-mail;
  - [x] **RF** - O usuário deve receber um e-mail com instruções de recuperação de senha;
  - [x] **RF** - O usuário deve poder resetar sua senha;
  - [x] **RNF** - Utilizar Ethereal para testar envios em ambiente de dev;
  - [x] **RNF** - Utilizar Amazon SES para envios em produção;
  - [x] **RNF** - O envio de e-mails deve acontecer em segundo plano (background job);
  - [x] **RN** - O link enviado por email para resetar senha, deve expirar em 2h;
  - [x] **RN** - O usuário precisa confirmar a nova senha ao resetar sua senha;
- [x] Atualização do perfil;
  - [x] **RF** - O usuário deve poder atualizar o seu nome, email e senha;
  - [x] **RN** - O usuário não pode alterar seu email para um email já utilizado;
  - [x] **RN** - Para atualizar sua senha, o usuário deve informar a senha antiga;
  - [x] **RN** - Para atualizar sua senha, o usuário precisa confirmar a nova senha;
- [x] Painel do prestador;
  - [x] **RF** - O usuário deve poder listar seus agendamentos de um dia específico;
  - [x] **RF** - O prestador deve receber uma notificação sempre que houver um novo agendamento;
  - [x] **RF** - O prestador deve poder visualizar as notificações não lidas;
  - [x] **RNF** - Os agendamentos do prestador no dia devem ser armazenados em cache;
  - [x] **RNF** - As notificações do prestador devem ser armazenadas no MongoDB;
  - [x] **RNF** - As notificações do prestador devem ser enviadas em tempo-real utilizando Socket.io;
  - [x] **RN** - A notificação deve ter um status de lida ou não-lida para que o prestador possa controlar.
- [x] Agendamento de serviços;
  - [x] **RF** - O usuário deve poder listar todos prestadores de serviço cadastrados;
  - [x] **RF** - O usuário deve poder listar os dias de um mês com pelo menos um horário disponível de um prestador;
  - [x] **RF** - O usuário deve poder listar horários disponíveis em um dia específico de um prestador;
  - [x] **RF** - O usuário deve poder realizar um novo agendamento com um prestador;
  - [x] **RNF** - A listagem de prestadores deve ser armazenada em cache;
  - [x] **RN** - Cada agendamento deve durar 1h exatamente;
  - [x] **RN** - Os agendamentos devem estar disponíveis entre 8h às 18h (Primeiro às 8h último às 17h);
  - [x] **RN** - O usuário não pode agendar em um horário já ocupado;
  - [x] **RN** - O usuário não pode agendar em um horário que já passou;
  - [x] **RN** - O usuário não pode agendar serviços consigo mesmo;

### :rocket: Tecnologias:
- [TypeScript](https://www.typescriptlang.org/)
- [NodeJS](https://nodejs.org/en/)
- [React](https://reactjs.org/ "ReactJS")
- [React Native](https://reactnative.dev/ "React Native")
 
<i id="contribuir"></i>

## :link: Como contribuir

- Faça um **fork** do projeto;
- Crie uma nova branch com as suas alterações: `git checkout -b my-feature`
- Salve as alterações e crie uma mensagem de commit contando o que você fez:`git commit -m "feature: My new feature"`
- Envie as suas alterações: `git push origin my-feature`

> Caso tenha alguma dúvida confira este [guia de como contribuir no GitHub](https://github.com/firstcontributions/first-contributions)

## :memo: Licença
Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.


---

<h4 align="center">
    Feito com ❤ por <a href="https://www.linkedin.com/in/julio-nery/" target="_blank">Júlio Nery</a>!
    <g-emoji class="g-emoji" alias="wave" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f44b.png">👋</g-emoji>
</h4>
