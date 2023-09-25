---
date: 2023-09-25
authors: [gabrielbdornas]
categories:
  - DCD
---

# Criação de usuário para adminstração geral GitHub

Quando a organização [SUGES-MG](https://github.com/suges-mg/) foi criada apenas meu usuário GitHub (`gabrielbdornas`) estava ligado a mesma como `owner`.
Após minha experiência na [Diretoria Central de Transparência Ativa - DCTA/CGE](https://cge.mg.gov.br/a-cge/quem-e-quem/subcontroladoria-de-transparencia-e-integridade#:~:text=DIRETORIA%20DE%20TRANSPAR%C3%8ANCIA%20ATIVA) entendi que deixar contas de organizações vinculadas apenas a servidores não é uma boa prática, **principalmente no quisito troca de equipe**.

<!-- more -->

Se uma organização estiver vinculada a apenas um `owner` (como era o caso da [SUGES-MG](https://github.com/suges-mg/)) caso este saia da equipe a transição da adminstração da conta será muito mais difícil.
Criar uma conta geral para isso deixa os processos de transição de servidores mais suaves.
Nestes casos, no lugar de indicar novo(s) `onwer` basta remover (se for o caso) o acesso do servidor que está deixando a equipe.

Outro ponto a ser destacado é a criação e utilização de `tokens`, principalmente para rodar `actions`, em contas pessoais.
Caso um servidor saia da equipe, por medida de segurança, o mais correto a ser feito e que este revogue todos os `tokens` de sua conta que estejam sendo utilizados na organização que ele não mais fará parte.
Quando isso ocorrer `actions` que dependem destes `tokens` não mais funcionarão, quebrando assim rotinas já estáveis.
Sendo assim, a proposta é gerar `tokens` no novo usuário criado para este fim e não não mais em contas pessoais.

O usuário [dcd-github-admin](https://github.com/dcd-github-admin) foi criado para esta finalidade.
Ele está vinculado a conta de e-mail `simplificacao`.
Pessoas da equipe que precisem gerenciar este usuário devem pedir acesso a essa caixa enviando um e-mail para `suporteti.ca@lanlink.com.br`.
