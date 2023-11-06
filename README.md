<h1> API REST - Gerenciador Financeiro 📊💰 </h1>

<p> Esse repositório demonstra os códigos desenvolvidos para finalização do Modulo 03 do curso de Desenvolvimento Back-End pela instituição Cubos Academy. Fomos desafiadas pela Cubos Academy a desenvolver um sistema de gerenciamento financeiro API REST com persistência de dados, criptogragia de senha e geração de token para os usuários logados no sistema 🤯🎯 </p>
<p>
<li> Desenvolvemos 12 rotas que buscam realizar operações básicas de um gerenciador financeiro; </li>
<li> Criamos três controladores (transações, categorias e usuários) para armazenamento dos códigos das rotas criadas. </li> 
<li> Criamos sete intermediários para a proteção das rotas criadas. </li> 
<li> As rotas possuem como tipo de resquisição req.body, req.params, req.headers e/ou req.params; </li>
<li> Todas rotas possuem a exibição de um status code adequado a resposta da requisição, seja do tipo bem-sucedida ou mal-sucedida; </li>
</p>
<p> 👩🏽‍💻✨Este projeto foi realizado em parceria com Yara Garcia <a href = "https://github.com/Yara-Garcia"> Acesse seu perfil </a> </p>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> 👩🏽‍🔧 Linguagens e Ferramentas </h2>
<li> JAVASCRIPT </li>
<li> NODEJS </li>
<li> PROTOCOLO HTTP </li>
<li> JSON </li>
<li> BIBLIOTECAS NODEMON E EXPRESS </li>
<li> BIBLIOTECA NODE-POSTGRES </li>
<li> BIBLIOTECA BCRYPT </li>
<li> BIBLIOTECA JWT </li>
<li> PostgreSQL e BEEKEEPER </li>
<li> INSOMNIA </li>
<li> VSCODE </li>
<li> GIT </li>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 01: Cadastrar um Usuário 👵🏽🧔🏽 </h2>
<div>
  <h3> POST /usuario </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/a9d538e9-13a8-4494-90b0-d492ee550d41">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Cria um novo usuário cujo número (ID) é único; </li>
<li> Para que seja possível o cadastro de um novo usuário, é necessário verificar se todos os campos foram informados (todos são obrigatórios);</li>
<li> Não é possível a criação de um novo usuário com o mesmo e-mail de usuário anteriormente cadastrado no sistema de banco de dados; </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 02: Realizar Login ✅👨🏽‍💻 </h2>
<div>
  <h3> POST /login </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/3c6d78d2-f343-499f-ae81-171c0bde17b4">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Realiza o login do usuário no sistema para que seja possível a realização de suas operações financeiras; </li>
<li> O usuário somente realiza login no sistema se o e-mail e senha informadas conferem com o cadastro do usuário;</li>
<li> Com o acesso do usuário ao sistema, é gerado um token de acesso. Este token é utilizado como req.headers para validação de acesso; </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 03: Detalhar usuário 🕵🏽‍♀️🧾 </h2>
<div>
  <h3> GET /usuario </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/f0135d5e-dc88-4c39-ade2-f9de4d0482ef">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Detalha as informações de um usuário; </li>
<li> Verifica se o usuário está com cadastro no sistema;</li>
<li> Token utilizado como req.headers para validação de acesso; </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 04: Atualizar usuário ✅🔄 </h2>
<div>
  <h3> PUT /usuario </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/c3a6e859-feca-4ba9-b929-4d2673e8fcbb">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Atualiza as informações de um usuário; </li>
<li> Não permite o uso de um e-mail utilizado por outro usuário cadastrado no banco de dados;</li>
<li> Token utilizado como req.headers para validação de acesso. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 05: Listar categorias de transações 🧾💰 </h2>
<div>
  <h3> GET /categoria </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/eb454e99-481e-4353-848e-f7945f122ea8">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Lista todas categorias disponíveis para classificação das transações do usuário; </li>
<li> Token utilizado como req.headers para validação de acesso. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 06: Cadastrar transação ✅💳 </h2>
<div>
  <h3> POST /contas </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/aeea8025-7e62-4ca9-8d35-f1d797b6b970">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Cria uma nova transação financeira cujo número (ID) é único; </li>
<li> Verifica se todos os campos foram informados (todos são obrigatórios); </li>
<li> Verifica se o ID da transação existe; </li>
<li> Padroniza a escrita do campo tipo; </li>
<li> Token utilizado como req.headers para validação de acesso. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota 07: Exibir transações financeiras do usuário logado ✅🧾 </h2>
<div>
    <h3> GET /transacao </h3>
  <img src = "https://github.com/taiscostaeng/sistema-gerenciador-financeiro-api-rest/assets/138815703/cfbd0d30-f4a7-45a4-91bf-b403cd91c897">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Exibe todas transações financeiras do usuário; </li>
<li> Token utilizado como req.headers para validação de acesso. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Atualizar usuário da conta bancária ✅🔄 </h2>
<div>
  <h3> PUT /contas/:numeroConta </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/9fce1a65-72a6-476d-9645-2f61a5356736">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Atualiza os dados do usuário de uma conta bancária; </li>
<li> Verifica se todos os campos foram informados (todos são obrigatórios); </li>
<li> Verifica se o numero da conta passado como parametro na URL é válida; </li>
<li> Verifica se o CPF e e-mail já foram vinculados a um outro usuário; </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Excluir conta 🗑💰 </h2>
<div>
  <h3> DELETE /contas/:numeroConta </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/56e5f342-669b-4ef0-ab3e-3dcb871ae526">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li>Verifica se o numero da conta passado como parametro na URL é válido; </li>
<li>Permite apenas a exclução da conta bancária se o saldo for R$0,00; </li>
<li>Exclui a conta do objeto. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Depositar 💰🤑 </h2>
<div>
  <h3> POST /transacoes/depositar </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/3c70ae5d-4463-430c-82b4-3cffaf5d174d">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Verifica se o numero da conta e o valor do deposito foram informados no body; </li>
<li> Verifica se a conta bancária informada existe; </li>
<li> Não permite depósitos com valores negativos ou zerados; </li>
<li> Soma o valor de depósito ao saldo da conta; </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Sacar 💸🤑 </h2>
<div>
  <h3> POST /transacoes/sacar </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/274a0df8-59a3-459c-98f1-4c0959951efa">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Verifica se o numero da conta, o valor do saque e a senha foram informados no body; </li>
<li> Verifica se a conta bancária informada existe; </li>
<li> Verifica se a senha informada é uma senha válida para a conta informada; </li>
<li> Verifica se há saldo disponível para saque; </li>
<li> Subtrai o valor sacado do saldo da conta encontrada; </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Saldo 💲🤑 </h2>
<div>
  <h3> GET /contas/saldo </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/a191b84e-7858-403b-960f-e1c5d6ebb121">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Verifica se o numero da conta e a senha foram informadas (passado como query params na url); </li>
<li> Verifica se a conta bancária informada existe; </li>
<li> Verifica se a senha informada é uma senha válida; </li>
<li> Exibe o saldo da conta bancária em questão. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Extrato Bancário 🧾💲 </h2>
<div>
  <h3> GET /contas/extrato </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/a7679425-0bca-459e-8bda-8c15f555a8f2">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Verifica se o numero da conta e a senha foram informadas (passado como query params na url); </li>
<li> Verifica se a conta bancária informada existe; </li>
<li> Verifica se a senha informada é uma senha válida; </li>
<li> Retorna a lista de transferências, depósitos e saques da conta em questão.</li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> Rota XX: Transferência entre Contas 💰🤑 </h2>

<div>
  <h3> POST /transacoes/transferir </h3>
  <img src = "https://github.com/taiscostaeng/sistema-bancario-api-rest/assets/138815703/dd402811-2d62-4f3f-bf9c-02d099289817">
</div>

<div>
<h3> O quê essa rota faz? 🤔 </h3>
<li> Verifica se o número da conta de origem, de destino, senha da conta de origem e valor da transferência foram informados no body; </li>
<li> Verifica se a conta bancária de origem informada existe; </li>
<li> Verifica se a conta bancária de destino informada existe; </li>
<li> Verifica se a senha informada é uma senha válida para a conta de origem informada; </li>
<li> Verifica se há saldo disponível na conta de origem para a transferência; </li>
<li> Subtrai o valor da transfência do saldo na conta de origem; </li>
<li> Soma o valor da transferência no saldo da conta de destino. </li>
</div>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> ✨😊 Você quer contribuir com esse projeto? </h2>
<li> Primeiro, você precisa realizar o fork desse projeto; </li>
<li> Em seguida, configure o seu servidor. Você pode realizar o passo a passo seguindo esse <a href = "https://github.com/taiscostaeng/configuracao-servidor/tree/master"> link aqui </a> </li>
<li> Depois, você pode realizar as alterações no código; </li>
<li> Por fim, você precisa realizar o Pull Request (PR) para esse repositório; </li>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
<h2> 🎖🏆 Funcionalidades do Projeto </h2>
Esse projeto foi desenvolvido para executar as funções básicas de um sistema bancário:
<ol>
  <li> Criar conta bancária </li>
  <li> Listar todas contas bancárias cadastradas </li>
  <li> Atualizar usuário </li>
  <li> Deletar conta </li>
  <li> Realizar depóstio </li>
  <li> Realizar saque </li>
  <li> Consultar saldo </li>
  <li> Consultar extrato bancário </li>
  <li> Realizar transferências entre contas bancárias </li>
</ol>
