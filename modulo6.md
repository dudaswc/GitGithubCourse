## Módulo 6 — Extras

### Criando o `.gitignore`

O arquivo `.gitignore` é utilizado para informar ao Git **quais arquivos ou pastas não devem ser versionados**.

Isso é útil para evitar enviar arquivos desnecessários ou sensíveis para o repositório, como:

- arquivos temporários
- dependências
- arquivos de configuração local
- logs

Exemplo de `.gitignore`:

```gitignore
node_modules/
.env
*.log
dist/
````

---

### Git Stash

O `git stash` permite **guardar temporariamente alterações que ainda não foram commitadas**, deixando o diretório de trabalho limpo.

Guardar alterações:

```bash
git stash
```

Ver stashes salvos:

```bash
git stash list
```

Recuperar alterações guardadas:

```bash
git stash apply
```

Remover um stash após utilizá-lo:

```bash
git stash drop
```

---

### Versionando com Tags

As **tags** são usadas para marcar versões importantes de um projeto, como releases.

Criar uma tag:

```bash
git tag v1.0
```

Listar todas as tags:

```bash
git tag
```

Enviar tags para o repositório remoto:

```bash
git push origin v1.0
```

Enviar todas as tags:

```bash
git push origin --tags
```

---

### Git Revert

O `git revert` é utilizado para **desfazer alterações feitas por um commit**, criando um novo commit que cancela o anterior.

Exemplo:

```bash
git revert ID_DO_COMMIT
```

Isso mantém o histórico do projeto seguro, sem apagar commits anteriores.

---

### Apagando Tags e Branches Remotos

Apagar uma branch remota:

```bash
git push origin --delete nome-da-branch
```

Apagar uma tag local:

```bash
git tag -d nome-da-tag
```

Apagar uma tag remota:

```bash
git push origin --delete nome-da-tag
```

Esses comandos ajudam a manter o repositório organizado, removendo branches ou versões que não são mais necessárias.

