
## Módulo 3 — Essencial do Git

### Inicializando um repositório

Para começar a versionar um projeto com Git, é necessário inicializar um repositório dentro da pasta do projeto.

```bash
git init
````

Esse comando cria um repositório Git local que passará a controlar as versões dos arquivos.

---

### Usando o editor do terminal

Em alguns momentos o Git abre um editor de texto no terminal (geralmente para escrever mensagens de commit ou editar configurações).

No editor padrão (como **Vim**):

* Pressione `i` para entrar no modo de edição
* Escreva a mensagem desejada
* Pressione `ESC`
* Digite `:wq` para salvar e sair

---

### Ciclo de vida dos arquivos no Git

Os arquivos dentro de um repositório passam por alguns estados:

**Untracked**
Arquivo novo que o Git ainda não está monitorando.

**Modified**
Arquivo que foi modificado após o último commit.

**Staged**
Arquivo preparado para ser incluído no próximo commit.

**Committed**
Arquivo salvo no histórico do repositório.

Comandos principais:

Adicionar arquivo para stage:

```bash
git add nome-do-arquivo
```

Adicionar todos os arquivos:

```bash
git add .
```

Criar um commit:

```bash
git commit -m "mensagem do commit"
```

Verificar o status dos arquivos:

```bash
git status
```

---

### Visualizando os logs

O comando `git log` permite visualizar o histórico de commits do repositório.

```bash
git log
```

Ele mostra informações como:

* autor do commit
* data
* mensagem
* identificador do commit (hash)

Versão resumida:

```bash
git log --oneline
```

---

### Visualizando diferenças (diff)

O comando `git diff` mostra as diferenças entre versões de arquivos.

```bash
git diff
```

Ele permite ver exatamente **o que foi alterado no código antes de fazer um commit**.

---

### Desfazendo alterações

Desfazer modificações em um arquivo antes do commit:

```bash
git checkout -- nome-do-arquivo
```

Remover arquivo da área de stage:

```bash
git reset nome-do-arquivo
```

Esses comandos ajudam a corrigir erros antes que as alterações sejam registradas no histórico do projeto.

```

