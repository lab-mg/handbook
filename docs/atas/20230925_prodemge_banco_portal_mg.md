# Acesso ao banco de dados do Portal MG - PRODEMGE

**Data:** 25/09/2023

## Pauta
- Acesso ao banco de dados do Portal MG.

## Participantes
- Gabriel
- Linda
- Fabiana
- Rogério

## Assuntos tratados
- Gabriel inicio contextualizando a reunião com [Diniz e Damião](../20230918_apresentacao_canais_digitais_mapa_transformacao)[^1].
- Rogério explicou que Portal MG é construído com ferramenta [CMS drupal](https://www.drupal.org/), aonde cada campo é uma tabela. Teremos então que realizar vários `joins` para conseguir organizar os dados para publicação no PdA.
- Banco de dados do Portal MG é MySql
- Rogério comentou que a criação de um web service também poderia acontecer, mas preferimos seguir com a opção de acesso direto ao banco. Isso dará mais flexibilidade no futuro, caso seja necessário acessar mais alguma informação.
- Rogério comentou do campo `timestamp` que ajudará a bascar apenas registros com atualizações durante processo ETL.
- Gabriel e Rogério reforçaram que o acesso criado será apenas de visualização.
- Rogério comentou que provavelmente iremos acessar o banco de produção e Gabriel informou que rotina rodará de madrugada.
- Gabriel enviará um e-mail para Damião falando da reunião e formalizando o pedido de acesso.
- Todos da reunião serão colocados em cópia.

## Dúvidas
- Sem dúvidas.

## Ideias
- Sem ideias.

## Ações
- Gabriel enviará e-mail para Damião solicitando formalização do pedido na PRODEMGE.
- Rogério já analisará quem deverá realizar a liberação.

[^1]: Rogério comentou que o site da Nasa é construído nesta ferramenta, com mais de uma instância.
