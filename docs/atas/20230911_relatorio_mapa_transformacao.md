# Mapa de Transformação

**Data:** 12/09/2023

## Participantes:

- Augusta Cora
- Gabriel

## Assuntos tratados

- Reunião sugerida durante [conversa de apresentação da colega Cora](../20230911_apresentacao_augusta_cora).
- Apresentação do fluxo para geração do [Mapa de Transformação](https://app.powerbi.com/view?r=eyJrIjoiNmQzZDMxZGMtNGM0OC00YWJmLWIxMjctMTM0OWJjMTAyZWNmIiwidCI6ImU1ZDNhZTdjLTliMzgtNDhkZS1hMDg3LWY2NzM0YTI4NzU3NCJ9&pageName=ReportSection8b08997a641ffd25674f)[^1].
- Foco nas dúvidas registradas na [última reunião](../20230911_apresentacao_augusta_cora/#duvidas):
    - Quem dá manutenção no Portal MG? e Portal MG é de responsabilidade da Diretoria Central de Canais Digitais?
        - Sim é a Diretoria Central de Canais Digitais a [responsável pelo Portal MG](https://www.almg.gov.br/legislacao-mineira/texto/DEC/48636/2023/#:~:text=I%20%E2%80%93-,gerenciar,-os%20canais%20corporativos).
    - Por que acesso ao relatório é feito apenas na CAMG?
        - Provavelmente por motivos de segurança.
    - Slide 4 mostra que a planilha é enviada para outros setores. Quais setores e quais são as análises feitas por eles?
        - A própria Diretoria Central de Canais Digitais para geração das demais informações no [Mapa de Transformação](https://app.powerbi.com/view?r=eyJrIjoiNmQzZDMxZGMtNGM0OC00YWJmLWIxMjctMTM0OWJjMTAyZWNmIiwidCI6ImU1ZDNhZTdjLTliMzgtNDhkZS1hMDg3LWY2NzM0YTI4NzU3NCJ9&pageName=ReportSection8b08997a641ffd25674f)[^1]
    - Existe algum dado sensível neste relatório que não pode ser divulgado?
        - A princípio não, considerando, inclusive, que as informações já são disponibilizadas em formato de dashboard.
    - O que é DCAE?
        - Antigo nome da Diretoria Central de Canais Digitais.
    - Quanto tempo é gasto com esta atividade mensalmente (estimativa)?
        - 3 horas somente na Diretoria Central de Desburocratização.
    - Qual ganho esperado ao final da automatização do mesmo?
        - A Geração [Mapa de Transformação](https://app.powerbi.com/view?r=eyJrIjoiNmQzZDMxZGMtNGM0OC00YWJmLWIxMjctMTM0OWJjMTAyZWNmIiwidCI6ImU1ZDNhZTdjLTliMzgtNDhkZS1hMDg3LWY2NzM0YTI4NzU3NCJ9&pageName=ReportSection8b08997a641ffd25674f)[^1] de maneira automática liberará tempo para o trabalho de fato, que é a geração de valor no processo de simplificação a partir da análise e não a tabulação de dados.
- Maneira atual de extrair relatório do Portal MG:
    - Coluna `DocsEmitidosAdmPub` é preenchido com `-` quando novo serviço é cadastrado, exigindo assim esta análise.
    - Análise não foi feita por um período.
    - Atualmente dashboard é alimentado por uma planilha compartilhada em rede.
    - Após finalização análise em arquivo excel as informações são passadas para o sistema, que emite outro relatório com a consolidação da informação.
- Novo processo:
    - Cadastro de novas etapas (em serviços) exigirá a seleção de documentos pré-cadastrados e não um campo aberto.
    - Este pré-cadastro já trará a informação de documento emitido pela Administração Pública.
    - Novo processo ainda não foi totalmente implantado. Exige treinamento dos editores de conteúdo.
    - Migrar etapas (em serviços) anteriormente cadastrados para a nova forma (documentos pré-cadastrados).

## Dúvidas
- Novo processo de cadastro de documentos dará opção de campo aberto? Se sim, como editor de conteúdo solicitará cadastro de documento inexistente?
- Base de dados Portal MG é guardada pela PRODEMGE?

## Ideias
- Conforme já registrado na [ata anterior](../20230911_apresentacao_augusta_cora/#ideias), podemos publicar a base de dados do Portal MG no PdA. Desta forma, não seria mais necessário gerar relatórios para alimentar [Mapa de Transformação](https://app.powerbi.com/view?r=eyJrIjoiNmQzZDMxZGMtNGM0OC00YWJmLWIxMjctMTM0OWJjMTAyZWNmIiwidCI6ImU1ZDNhZTdjLTliMzgtNDhkZS1hMDg3LWY2NzM0YTI4NzU3NCJ9&pageName=ReportSection8b08997a641ffd25674f)[^1]. Para isso será necessário criar um processo ETL para atualizar diariamente o PdA.

[^1]: Também disponível na página [Minas Atende](https://www.mg.gov.br/pagina/minas-atende) e anteriormente desenvolvido com a ferramenta [lookerstudio](https://lookerstudio.google.com/reporting/4c83d18e-b293-43a7-8707-d2e8834fcc0f/page/dB2dB).
