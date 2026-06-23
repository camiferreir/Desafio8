# README – Atividade: Cookies e Sessions no PHP

## Descrição

Este projeto foi desenvolvido com base na Apostila 7 – Cookies e Sessions no PHP. O objetivo é demonstrar, na prática, como o PHP consegue manter informações do usuário entre diferentes páginas utilizando Cookies e Sessions.

Foram implementados dois exemplos completos:

* Sistema de Login utilizando Sessions e Cookies;
* Preferência de Tema (Claro/Escuro) utilizando Cookies.

---

# Exemplo 1 – Sistema de Login

## Objetivo

Criar um sistema simples de autenticação utilizando Sessions para controlar o acesso do usuário e Cookies para lembrar o nome de usuário no formulário de login.

## Estrutura de Arquivos

login-exemplo/

├── index.php

├── validar.php

├── dashboard.php

└── sair.php

## Funcionamento

### index.php

* Exibe o formulário de login;
* Mostra mensagens de erro quando necessário;
* Preenche automaticamente o campo de usuário caso exista o cookie "usuario";
* Permite marcar a opção "Lembrar-me".

### validar.php

* Recebe os dados enviados pelo formulário;
* Verifica se as credenciais estão corretas;
* Cria a sessão do usuário autenticado;
* Salva ou remove o cookie de usuário conforme a escolha da opção "Lembrar-me";
* Redireciona o usuário para o dashboard.

### dashboard.php

* Página protegida;
* Permite acesso somente para usuários autenticados;
* Exibe o nome do usuário logado;
* Informa quando o login foi salvo por meio do cookie;
* Disponibiliza o botão de logout.

### sair.php

* Encerra a sessão ativa;
* Remove os dados da sessão;
* Redireciona o usuário para a página de login.

## Credenciais para Teste

Usuário: admin

Senha: 1234

---

# Exemplo 2 – Preferência de Tema

## Objetivo

Permitir que o usuário escolha entre o tema claro e o tema escuro, salvando sua preferência em um cookie para que ela seja aplicada automaticamente nas próximas visitas.

## Estrutura de Arquivos

tema-com-cookies/

├── index.php

├── set_tema.php

└── style.css

## Funcionamento

### index.php

* Verifica se existe um cookie chamado "tema";
* Define o tema padrão como claro;
* Aplica automaticamente o tema salvo;
* Exibe botões para alterar a preferência.

### set_tema.php

* Recebe o tema escolhido pelo usuário;
* Salva a preferência em um cookie válido por 30 dias;
* Redireciona novamente para a página principal.

### style.css

* Define os estilos do tema claro;
* Define os estilos do tema escuro;
* Organiza visualmente a página.

---

# Conceitos Utilizados

## Cookies

Cookies são pequenos arquivos armazenados no navegador do usuário. Eles permitem guardar informações simples, como preferências de tema ou dados de preenchimento automático.

### Vantagens

* Fácil implementação;
* Persistem entre visitas;
* Úteis para preferências do usuário.

### Desvantagens

* Menor segurança;
* Podem ser visualizados e alterados pelo usuário;
* Possuem limite de tamanho.

---

## Sessions

Sessions armazenam informações diretamente no servidor, utilizando um identificador único enviado ao navegador.

### Vantagens

* Maior segurança;
* Ideais para autenticação;
* Não expõem dados sensíveis ao usuário.

### Desvantagens

* Dependem do servidor;
* São temporárias e podem expirar.

---

# Conclusão

A utilização de Cookies e Sessions é essencial no desenvolvimento de aplicações web com PHP. Enquanto os Cookies permitem armazenar preferências e informações simples no navegador, as Sessions garantem maior segurança ao controlar dados importantes, como autenticação de usuários.

Com esta atividade foi possível compreender como o PHP mantém o estado do usuário entre diferentes requisições HTTP, aplicando esses conceitos em exemplos práticos de login e personalização de interface.
