---
comments: true
tags:
  - Modelos
---

# Métricas automatizações - Microsoft

- **Data:** 20/10/2023

## Pauta
- Entender melhor métricas relatórios Power Automate.
- [Reunião anterior](../20231004_relatorios_automate).

## Participantes
- André
- Lucas
- Banes
- Gabriel
- Tiago
- Ivan - Representando Henrique
- Tiago Ferreira (Microsoft)


## Assuntos tratados
- Relatório robôs desktop:
    - Usuário.
    - Número de vezes que rodou.
    - Tempo que cada iteração levou para rodar.
    - Código fonte do robô.
- Tiago explicou:
    - Tenents: 
        - Isolamento de inquilinos. 
        - Cada tenent é uma empresa diferente. 
        - Tenents não acessão outros pela questão de segurança e isolamento.
        - Podemos utilizar conectores para liberar as informações de um tenent em outro. Estabelecer confianças. 
        - **Precisamos saber quais os tenents do governo para pedir acesso**.
        - Lucas perguntou Tiago se ele teria esta lista, mas ele respondeu que não. Não necessariamente as vendas foram feitas pelo mesma empresa. Mas ele e Ivan ficaram de tentar enviar esta lista.
    - Relatórios:
        - Ferramentas dão liberdade às equipes, mas podem ficar grandes demais.
        - [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit) (centro de excelência): Empacotar soluções para reaproveitamento em outros ambientes. Fazendo apenas adaptações.
        - [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit) uma vez configurado pode gerar os relatórios que necessitamos.
    - Mostrou tela do [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit) **e em um primeiro momento parece que é bem próximo do que precisamos**.
    - Instlação CoE é 100% web.
    - Mostrou como fazer as consultas nos relatórios de auditoria. Testar o link compliance.microsoft.com e Ivan conseguiu abrir a tela para uma demonstração na hora.
    - Terceira opção: Biblioteca powershell script (role audit log permission ou audit report e power automate admin):
        - [Documentação Power Shell](https://learn.microsoft.com/pt-br/power-platform/admin/powerapps-powershell).
        - [API Rest]() - Sem documentação enviada no momento da reunião.
- Perguntas:
    - Nosso plano atual dá direito a configuração do [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit)?
        - Único requisito são premiun, mas podemos 
    - Como faríamos esta configuração?
        - Material disponível possibilita instalação sem precisar da equipe Microsof.
    - Preciso do [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit) para os relatórios que estou pedindo? Não seria possível extrair isso de maneira mais simples?
        - Seria possível via scripts nos relatórios de auditoria. Uma espécie de consulta SQL.
    - Como operacionalizar:
        - Alguém que tem role Tenent admin.   
- [Relatório](https://cecad365-my.sharepoint.com/:x:/g/personal/x10426269_ca_mg_gov_br/EUNmoVs24GtCp-OVmibkmSIBfn3Rf9AK_GuWXjSQK25-qA?e=4%3A2xaZTW&fromShare=true&at=9&CID=7614e476-06a7-e6b8-11d7-8ed3066eba33) tirado por Ivan durante a reunião.

## Dúvidas
- Sem dúvidas.

## Ideias
- Sem ideias

## Ações
- Liberação de usuários com a Intendência. Banes pediria por e-mail.
- Estudo de como instalar [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit).
- Setup inicial [CoE](https://learn.microsoft.com/en-us/power-platform/guidance/coe/starter-kit).
- Tiago irá procurar e enviar documentação [API Rest]().
