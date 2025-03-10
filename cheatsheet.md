# Git Cheatsheet

## Configuração
```sh
$ git config --global user.name "Seu Nome"
$ git config --global user.email "seuemail@example.com"
$ git config --list
```

## Inicializando um repositório

No diretório do projeto que te interessa utilizar o versionamento com git, use o comando `git init`.

## Clonando um repositório

Caso o repositório de interesse já exista, use o comando `git clone` para cloná-lo num repositório local:

```sh
$ git clone <url-do-repositorio>
```

## Verificando status da branch

Caso queira verificar o status da branch atual (quais arquivos foram alterados, se existem arquivos na área de stage, se existem arquivos untracked, etc), use o comando `git status`.

## Adicionando arquivos à área de staging

Para adicionar arquivos à área de staging (i.e., os arquivos que serão salvos no próximo commit), você pode utilizar os comandos `git add` ou `git stage` (esse último não é tão utilizado, e tem a mesma funcionalidade do `git add`).

```sh
$ git add <arquivo> # adiciona um arquivo específico à área de staging
$ git add . # adiciona todos os arquivos a partir do diretório atual à área de staging.
```

## Removendo arquivos da área de staging

Caso você adicione algum arquivo para a área de staging sem querer, você pode usar o comando `git restore --staged <arquivo>` para removê-lo da área de staging.


## Salvando alterações

Após adicionar as alterações desejadas à área de staging, você pode utilizar o comando `git commit` para salvá-las. Isso abrirá um editor de texto (para verificar qual é, utilize o comando `git config core.editor`. Ele pode ser alterado posteriormente. Por padrão, é o `vim` ou o `nano`) para que você escreva uma mensagem (título e descrição) descrevendo brevemente quais alterações foram feitas pelo commit.

Ás vezes, você pode não querer escrever uma mensagem muito extensa. A flag `-m` ajuda: com ela, você escreve o título do commit direto no terminal, sem ter que abrir um editor de texto: 

```sh
$ git commit -m "Mensagem do commit"
```

## Criando uma branch

Quando você for realizar alguma alteração na base de código, o ideal é sempre fazer isso numa branch separada. Existem algumas maneiras diferentes para criar uma branch nova:

```sh
$ git checkout -b <nome-do-branch>
$ git switch -c <nome-do-branch>
```

## Listando branches existentes

Para verificar quais são as branches existentes, utilize o comando `git branch`. No caso, apenas as branches do repositório local (sua máquina) vão aparecer. Caso queira ver, também, as branches presentes no repositório remoto, utilize `git branch -a`.

## Trocando de branches

Analogamente à criação de branches, você pode utilizar os mesmos comandos para trocar de branch:

```sh
$ git checkout <nome-do-branch> 
$ git switch <nome-do-branch>
```

Observe, nesses casos, que não há uso de flags.

## Mesclar duas branches em uma só.

Para realizar a mescla, utilize o comando:

```sh
$ git merge <nome-do-branch>
```

## Integração com Repositório Remoto

Para integrar os dados do repositório remoto com o local (e vice-versa), você pode utilizar os comandos:

```sh
$ git pull origin <branch> # download do repositório remoto
$ git push origin <branch> # upload do repositório remoto
```

## Fazendo o download de alterações do repositório remoto

Para realizar esse download, utilize o comando `git fetch`. 
OBS: caso haja alteração na branch em que você está, ainda é necessário utilizar o comando `git pull` para integrá-las à sua branch local.

