---
tags:
  - Mapa de transformação
---

# Acompanhamento açõs fluxo de cadastro outros documentos

**Data:** 29/09/2023

## Pauta
- Acompanhamento ações do projeto:
    - Alinhamentos Cora:
        - Capacidade de rodadas de revisão com 20 serviços.
        - Iniciaremos a primeira rodada na próxima semana.
        - [Planilha preparada para o trabalho](https://cecad365.sharepoint.com/:x:/s/SCCA-DCAE-Canaiseletrnicos/ESNLHigw6WVJq1DG2Bucl38B20w4nSn5JSK4qV7l2GJ-OQ?e=97eBG9). Nova aba permitirá atualizarmos o relatório posteriormente sem perdermos os dados cadastrados durante a análise.
  - Retirar botão "outros documentos" (Bruno).
  - Pensar novo texto de orientação (Gabriel).
  - Desenhar o fluxo completo (Gabriel).
  - Pensar campos que hoje não aparecem para o cidadão (Gabriel).
  - Criar acessos Portal MG para equipe DCD (Inclusive ambiente de homologação) (Bruno).

## Participantes
- Gabriel
- Bruno
- Polyana
- Leyde

## Assuntos tratados
- Novo fluxo cadastro documento

```mermaid
flowchart TD
    1(Cadastro Evento)-->3
    3{Incluir documento?}
    3-->|Não|3.1
    3.1(Continua cadastro)
    3-->|Sim|3.2
    3.2{Documento pré-cadastrado?}
    3.2-->|Sim|3.1
    3.2-->|Não|3.2.1
    3.2.1[Salva cadastro como rascunho]-->3.2.2
    3.2.2[Envia e-mail simplificação]-->3.2.3
    3.2.3{Documento incluído?}
    3.2.3-->|Não|3.2.3.1
    3.2.3.1[Agarda retorno DCD]
    3.2.3.1-->3.2.3
    3.2.3-->|Sim|3.1
    3.1-->4
    4(Fim)
```

- Novo fluxo análise cadastro documento

```mermaid
flowchart TD
  1(E-mail recebido)-->2
  2{Documento pré-cadastrado?}
  2-->|Sim|2.1
  2.1[Orienta solicitante]
  2.1-->3
  3(Fim)
  2-->|Não|2.2
  2.2[Cadastra documento]-->2.3
  2.3[Informa solicitante]-->3

```

## Dúvidas
- Incluir dúvidas.

## Ideias
- Incluir ideias.

## Ações
- Incluir ações.
