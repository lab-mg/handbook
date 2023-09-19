# Treinamento Power Automate

**Data:** 19/09/2023

## Pauta
- Tempo estimado: 90 minutos.
- Pauta: Treinamento Power Automate.

## Participantes
- Gabriel
- Isabela
- Patrick

## Assuntos tratados
- Isabela realizou o treinamento Power Automate demostrando a automatização de um fluxo de consulta de CNPJS no [CAGEF](https://www.cagef.mg.gov.br/fornecedor-web/br/gov/prodemge/seplag/fornecedor/publico/index.zul). Fluxo envolvia:
  - Abrir planilha Excel com lista de CNPJs.
  - Abrir [página de consulta](https://www.cagef.mg.gov.br/fornecedor-web/br/gov/prodemge/seplag/fornecedor/publico/index.zul).
  - Criar um loop para passar todos os CNPJs listados.
  - Registrar no arquivo Excel aberto se o CNPJ consultado estava impedido ou não.
  - Salvar um print da tela consultada.
- Patrick e Gabriel não criaram o fluxo durante o treinamento pois não utilizam Windows como sistema operacional.
- Após treinamento Gabriel conseguiu realizar conexão Issues GitHub com Planner. Dificuldades foram registradas [neste issue](https://github.com/suges-mg/novas-ideias/issues/3):
    - Para que o trigger funcione, como o repositório desejado estava na organização [suges](https://github.com/suges-mg), foi necessário incluir o usuário `gabrielbdornas` como colaborador do projeto [mapa-transformacao](https://github.com/suges-mg/mapa-transformacao)[^1].
    - Para condicionar os issues de apenas um repositório a propriedade `repositório_url` tem que ser informada como o endereço do api GitHub (exemplo `https://api.github.com/repos/suges-mg/mapa-transformacao`).

## Dúvidas
- Sem dúvidas.

## Ideias
- Sem idéias

## Ações
- Sem ações.

[^1]: [Documentação Microsoft](https://learn.microsoft.com/en-us/connectors/github/#known-issues-and-limitations).
