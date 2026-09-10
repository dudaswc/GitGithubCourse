# Módulo 3 — Essencial do Git

## Inicializando um repositório

Para começar a versionar um projeto, é necessário inicializar um repositório dentro da pasta correspondente:

```bash
git init
```

Esse comando cria um repositório Git local que passa a controlar as versões dos arquivos.

## Usando o editor do terminal

Em alguns momentos, o Git abre um editor de texto no terminal, geralmente para escrever mensagens de commit ou editar configurações.

No Vim:

- Pressione `i` para entrar no modo de edição.
- Escreva a mensagem desejada.
- Pressione `Esc`.
- Digite `:wq` para salvar e sair.

## Ciclo de vida dos arquivos

Os arquivos de um repositório podem assumir os seguintes estados:

- **Untracked:** arquivo novo que o Git ainda não monitora.
- **Modified:** arquivo alterado após o último commit.
- **Staged:** arquivo preparado para o próximo commit.
- **Committed:** arquivo registrado no histórico do repositório.

Comandos principais:

```bash
git status
git add nome-do-arquivo
git add .
git commit -m "mensagem do commit"
```

## Visualizando os logs

O comando `git log` exibe o histórico de commits, incluindo autor, data, mensagem e identificador (hash):

```bash
git log
```

Para uma visualização resumida:

```bash
git log --oneline
```

## Visualizando diferenças

O comando `git diff` mostra o que foi alterado nos arquivos antes do commit:

```bash
git diff
```

## Desfazendo alterações

Para descartar alterações ainda não adicionadas à área de stage:

```bash
git restore nome-do-arquivo
```

Para remover um arquivo da área de stage sem apagar suas alterações:

```bash
git restore --staged nome-do-arquivo
```

Em versões e fluxos mais antigos do Git, também podem ser encontrados comandos como `git checkout -- nome-do-arquivo` e `git reset nome-do-arquivo`.
