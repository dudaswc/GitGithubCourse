## Módulo 5 — Ramificação (Branch)

### O que é uma branch e por que usar?

Uma **branch** é uma linha independente de desenvolvimento dentro de um repositório.

Ela permite trabalhar em novas funcionalidades, correções ou experimentos **sem alterar diretamente a versão principal do projeto**.

Vantagens de usar branches:

- Permite desenvolver funcionalidades separadamente
- Evita quebrar o código da versão principal
- Facilita o trabalho em equipe
- Organiza melhor o fluxo de desenvolvimento

A branch principal geralmente se chama **main** ou **master**.

---

### Criando uma branch

Para criar uma nova branch:

```bash
git branch nome-da-branch
````

Para criar e já mudar para a nova branch:

```bash
git checkout -b nome-da-branch
```

Ver todas as branches do repositório:

```bash
git branch
```

---

### Movendo e deletando branch

Trocar para outra branch:

```bash
git checkout nome-da-branch
```

Deletar uma branch:

```bash
git branch -d nome-da-branch
```

---

### Entendendo o merge

O **merge** é utilizado para **juntar o histórico de duas branches**.

Normalmente é usado quando uma funcionalidade foi desenvolvida em uma branch separada e precisa ser integrada à branch principal.

Exemplo:

```bash
git checkout main
git merge nome-da-branch
```

Isso incorpora as alterações da branch no projeto principal.

---

### Entendendo o rebase

O **rebase** é outra forma de integrar mudanças entre branches.

Ele reorganiza o histórico de commits, colocando os commits de uma branch **sobre outra**, criando um histórico mais linear.

Exemplo:

```bash
git checkout nome-da-branch
git rebase main
```

---

### Merge e Rebase na prática

**Merge**

* Junta duas branches
* Mantém o histórico completo
* Cria um commit de merge

**Rebase**

* Reorganiza o histórico de commits
* Deixa o histórico mais limpo
* Não cria commit extra de merge

Ambos são usados para integrar alterações entre branches, mas cada equipe pode escolher qual estratégia utilizar no fluxo de desenvolvimento.

