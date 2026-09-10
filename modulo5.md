# Módulo 5 — Ramificação (Branch)

## O que é uma branch e por que usar?

Uma **branch** é uma linha independente de desenvolvimento dentro de um repositório. Ela permite trabalhar em funcionalidades, correções ou experimentos sem alterar diretamente a versão principal.

Vantagens:

- Desenvolver funcionalidades separadamente.
- Proteger a versão principal.
- Facilitar o trabalho em equipe.
- Organizar o fluxo de desenvolvimento.

A branch principal geralmente se chama **main**.

## Criando uma branch

Para criar uma branch:

```bash
git branch nome-da-branch
```

Para criar e acessar a nova branch:

```bash
git switch -c nome-da-branch
```

O comando equivalente em fluxos mais antigos é `git checkout -b nome-da-branch`.

Para listar as branches:

```bash
git branch
```

## Movendo e deletando branches

Para trocar de branch:

```bash
git switch nome-da-branch
```

Para excluir uma branch local já integrada:

```bash
git branch -d nome-da-branch
```

## Entendendo o merge

O **merge** junta os históricos de duas branches. Para incorporar uma branch à principal:

```bash
git switch main
git merge nome-da-branch
```

## Entendendo o rebase

O **rebase** reaplica os commits de uma branch sobre outra base, criando um histórico mais linear:

```bash
git switch nome-da-branch
git rebase main
```

## Merge e rebase na prática

**Merge:**

- Junta duas branches.
- Preserva a estrutura do histórico.
- Pode criar um commit de merge.

**Rebase:**

- Reorganiza a base dos commits.
- Deixa o histórico mais linear.
- Reescreve commits e exige cuidado quando eles já foram compartilhados.

Cada equipe pode definir a estratégia mais adequada ao seu fluxo de trabalho.
