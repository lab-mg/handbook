---
date: 2023-10-06
authors: [gabrielbdornas]
comments: true
categories:
  - DCD
---

# Criando documentações incríveis

Eu não sei você, mas eu gosto bastante da ideia de criar documentos compartilhados.
Já tentei utilizar várias ferramentas, como as oferecidas no pacote Office e nunca me senti completamente satisfeito com o resultado.
Sempre pensei que a criação e o compartilhamento de informações deveriam ocorrer de maneira simplificada, mas somente após conhecer a filosofia [Docs as Code](https://www.writethedocs.org/guide/docs-as-code/) entendi como[^1].
Mas vamos direto para o mão na massa para deixar a coisa mais interessante.

<!-- more -->

## Pré-requisitos

- Como pré-requisitos temos:
    - [Conta no GitHub](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home).
    - Editor de texto (atualmente uso o VsCode).
    - Git.
    - Python.

## 101 Comandos

Os comandos demonstrados abaixo não são necessários caso você opte por utilizar ferramentas de interface gráfica, como o VsCode online disponível no GitHub[^2].

- Terminal:

```
$ pwd   # Mostra o diretório atual.
$ ls    # Lista arquivos e pastas do diretório atual.
$ cd    # Muda de diretorio. cd .. volta um diretório e cd pasta entra em alguma pasta.
$ mkdir # Cria uma pasta.
$ touch # Cria um arquivo.
$ cat   # Visualiza conteúdo de um arquivo.
$ rm    # Remove um arquivo. rm -rf remove uma pasta.
```

- Git:

```
$ init     # Inicia trabalho git.
$ status   # Informa se algo foi modificado.
$ log      # Mostra commits realizados.
$ add      # Adiciona um arquivo para ser commitado (salvo).
$ commit   # Salva o arquivo adicionado (versionamento).
$ checkout # Muda a branch.
$ clone    # Copia um repositório do GitHub localmente.
$ pull     # Atualiza repositório local com informações GitHub.
$ push     # Atualizada repositório GitHub com informações locais.
```

## Markdown

- Comandos gerais[^3]:
    - Cabeçalho: `#` (Vai de 1 a 6).
    - Negrito: `**`.
    - Itálico: `*`.
    - Citação: `>`.
    - Lista ordenada: `1. Primeiro`.
    - Lista não ordenada: `- Item`.
    - Código em linha: ``` ` ` ```.
    - Links: `[]()`.
    - Imagens: `![]()` ([imgur](https://imgur.com/)).

Markdown extendido:

- Tabelas: [Table Generator](https://www.tablesgenerator.com/markdown_tables)
- Lista de Tarefas: `- [ ] Tarefa 1` (Funciona comentário GitHub).
- Bloco de Código: ` ``` ```  `
- Emoji: :snake:
- Tachado: `~~tachado~~`
- Realçado: `==realçado==`
- [Mermaid](https://mermaid.js.org/intro/).

## Site estático

Misturando Markdown com ferramentas de geração de site estático conseguimos criar documentações incríveis.
A ferramentas de geração de site estático que vou demonstrar é o [Mkdocs](https://www.mkdocs.org/), em conjunto com seu tema mais famoso [material](https://squidfunk.github.io/mkdocs-material/).

Os comandos `mkdocs` são:

```
$ mkdocs new . # Para iniciar um projeto.
$ mkdocs build # Conversão md para html (prefiro comando serve).
$ mkdocs serve # Iniciar um servidor.
$ mkdocs gh-deploy # Fazer deploy.
$ mkdocs --help # Para pedir ajuda.
```

Para criarmos nosso primeiro site estático basta:

```
$ mkdir meu-primeiro-site-estatico
$ cd meu-primeiro-site-estatico
$ touch .gitignore # https://www.toptal.com/developers/gitignore/
$ touch requirements.txt # mkdocs on pypi
$ python -m venv venv # python3 -m venv venv no Linux
$ source venv/Scripts/activate # source venv/bin/activate
$ pip install -r requirements.txt
$ mkdocs new . # docs/ e mkdocs.yml
$ mkdocs serve # Testa mudanças ao vivo
# Inclua markdown no arquivo docs/index.md

# Incluindo Git
$ git init
$ git branch -M main # Pode ser configurado
$ git add .
$ git commit -m "Commit Inicial"
```

## Customizações

Conseguimos customizar o site com:

```
# Extensões para Markdown

$ pip install pymdown-extensions

# mkdocs.yml
markdown_extensions:
  - pymdownx.tasklist
  - pymdownx.emoji
  - pymdownx.mark      # Realçado
  - pymdownx.tilde     # Tachado
  - pymdownx.highlight # Códigos
```


```
# Mermaid - não precisa instalar nada via pip

# mkdocs.yml
markdown_extensions:
  - pymdownx.superfences:
      custom_fences:
        - name: mermaid
          class: mermaid
          format: !!python/name:pymdownx.superfences.fence_div_format

extra_css:
  - https://unpkg.com/mermaid@10.4.0/dist/mermaid.css
extra_javascript:
  - https://unpkg.com/mermaid@10.4.0/dist/mermaid.min.js
```

```
# Tema material

$ pip install mkdocs-material

# mkdocs.yml
theme:
  name: material
  palette:
    - scheme: default
      toggle:
        icon: material/weather-night
        name: Modo noturno
    - scheme: slate
      toggle:
        icon: material/weather-sunny
        name: Modo claro
```

```
# Personalização de blocos de código

hl_lines="" linenums="" title="Meu Arquivo.py"
```

## Publicação

Basta criar um repositório no GitHub e:

```
# Criar repositório GitHub
git remote add origin <repo-path>.git # camg utilizar https
git add .
git commit -m "Finaliza primeira versão"
git push origin main
mkdocs gh-deploy # Verifica página publicada.
```

Pronto.
Agora para deixar seu documento bonito basta seguir a documentação [material](https://squidfunk.github.io/mkdocs-material/).
Compartilhe seu trabalho com o maior número de colegas e porque não convidar todo mundo para colaborar[^3].

[^1]: Alguns exemplos de documentações feitas utilizando todas as ferramentas demonstradas no texto são este [Handbook](https://lab-mg.github.io/handbook) e [estas apresentações](https://lab-mg.github.io/reveal.js/)
[^2]: Para ter acesso basta apertar o ponto (`.`) na página inicial de qualquer repositóiro GitHub.
[^3]: Consulte também [esta apresentação](https://lab-mg.github.io/reveal.js/presentations/20230926_docs_as_code/index.html)!
