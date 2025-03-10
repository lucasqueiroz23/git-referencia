# Boas práticas

## Commits

### Commits atômicos

Um commit não deve conter várias mudanças ao mesmo tempo, mas apenas uma mudança. Isso não significa que apenas um arquivo deve ser alterado no commit, mas que ele representa uma única mudança encapsulada. Isso é bom porque, caso você queira voltar no tempo em um commit, você sabe exatamente aonde voltar. Além disso, o histórico de commits fica mais limpo. Não haverão commits gigantes. Também fica mais fácil de revisar Pull Requests com commits atômicos.

Ex: digamos que você está trabalhando numa issue em que você deve, num momento, atualizar a lista de usuários e, em outro, atualizar um log com erros. Ao invés de fazer isso tudo em um só commit, separe o seu trabalho em 2 commits.

### Co-authors

Muitas vezes, você não será o único a realizar um trabalho em um commit, mas trabalhará em equipe. O `co-author` é uma forma que serve para identificar co-autores de um commit na mensagem dele. Para adicionar um co-author em um commit, basta, no comentário do commit, adicionar o seguinte boilerplate:

`Co-authored-by: nome do co-autor <email>`.

Ex:
```
feat: adiciona Dockerfile para o back-end

Co-authored-by: José da Silva <josedasilva@gmail.com>
```

OBS: é importante que, entre o título e o comentário do commit, haja um espaçamento de, no mínimo, 2 linhas. 

### Mensagens descritivas

É importante que cada commit tenha uma descrição bem feita do que ele altera. Isso facilita muitas coisas (identificar um commit, revertê-lo, revisá-lo, etc).

Ex de commit com mensagem não descritiva:

```
Adicionando endpoint 
```

Ex de commit com mensagem descritiva (para o mesmo trabalho realizado):

```
Adiciona endpoint para busca de usuários cadastrados
```

Você também pode adicionar comentários, caso julgue necessário:
Ex:
```
Adiciona endpoint para busca de usuários cadastrados

Apenas os usuários com registro premium foram cadastrados, pois a conta de usuários comuns têm data de expiração.
```

### Uso de convenções e padrões de commits

Convenções e padrões de commits facilitam a leitura do histórico de commits. Eles devem ser decididos pelos mantenedores do repositório. Alguns exemplos de padrões: 

- **feat**: adiciona nova funcionalidade no projeto;
- **docs**: altera arquivos de documentação;
- **fix**: conserta algum bug ou realiza qualquer alteração que não é exatamente um feat;

Exemplo de uso:
```
docs: atualiza README com informações dos membros da equipe

Co-authored-by: fulaninho <fulano@hotmail.com>
```

### Mencionar issues

É possível rastrear um commit a partir de uma issue, desde que esse commit referencie a issue. Para realizar essa referência, basta utilizar o caracter `#` seguido do número da issue.
Ex:

```
feat: realiza tratamento de dados advindos da api externa

relativo à #23.
```

Na plataforma git, ao abrir a issue #23, pode-se encontrar uma referência para este commit.

## Pull Requests / Merge Requests

### Não altere 1000 arquivos em um MR

## Issues

## Políticas de branches
