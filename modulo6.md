# Módulo 6 — Extras

## Criando o `.gitignore`

O arquivo `.gitignore` informa ao Git quais arquivos ou pastas não devem ser versionados. Isso ajuda a evitar o envio de dependências, arquivos temporários, configurações locais, logs e dados sensíveis.

Exemplo:

```gitignore
node_modules/
.env
*.log
dist/
```

## Git stash

O `git stash` guarda temporariamente alterações ainda não commitadas e deixa o diretório de trabalho limpo:

```bash
git stash
git stash list
git stash apply
git stash drop
```

O comando `git stash pop` também recupera as alterações e remove o stash da lista quando a aplicação é concluída.

## Criando aliases

Aliases permitem criar atalhos para comandos utilizados com frequência. Por exemplo:

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.lg "log --oneline"
```

Depois disso, `git st`, `git co` e `git lg` passam a executar os comandos configurados.

## Versionando com tags

Tags marcam pontos importantes do histórico, como versões e releases:

```bash
git tag v1.0
git tag
git push origin v1.0
git push origin --tags
```

## Git revert

O `git revert` desfaz as alterações de um commit por meio da criação de um novo commit, preservando o histórico:

```bash
git revert ID_DO_COMMIT
```

## Apagando tags e branches remotas

Para excluir uma branch remota:

```bash
git push origin --delete nome-da-branch
```

Para excluir uma tag local:

```bash
git tag -d nome-da-tag
```

Para excluir uma tag remota:

```bash
git push origin --delete nome-da-tag
```
