# Módulo 4 — Repositórios Remotos

## Criando um repositório no GitHub

Para armazenar e compartilhar projetos remotamente, podemos criar um repositório no GitHub:

1. Acessar a conta no GitHub.
2. Clicar em **New repository**.
3. Definir o nome do repositório.
4. Escolher entre público ou privado.
5. Clicar em **Create repository**.

## Criando e adicionando uma chave SSH

A chave SSH permite conectar o computador ao GitHub de forma segura.

Para gerar uma chave:

```bash
ssh-keygen -t ed25519 -C "seuemail@email.com"
```

Para visualizar e copiar a chave pública:

```bash
cat ~/.ssh/id_ed25519.pub
```

Depois, no GitHub:

1. Acessar **Settings**.
2. Selecionar **SSH and GPG keys**.
3. Clicar em **New SSH key**.
4. Colar a chave pública.

## Ligando um repositório local a um remoto

Para conectar um repositório local ao GitHub:

```bash
git remote add origin URL_DO_REPOSITORIO
```

Para verificar a conexão:

```bash
git remote -v
```

## Enviando mudanças para o repositório remoto

No primeiro envio para a branch principal:

```bash
git push -u origin main
```

Nos próximos envios, geralmente basta utilizar:

```bash
git push
```

Para trazer alterações do repositório remoto:

```bash
git pull
```

## Clonando repositórios remotos

Clonar significa baixar uma cópia completa de um repositório para o computador:

```bash
git clone URL_DO_REPOSITORIO
```

## Fazendo fork de um projeto

Um **fork** é uma cópia de um repositório de outra pessoa para a própria conta. Ele é muito utilizado em projetos open source para experimentar modificações e propor contribuições ao projeto original.

Para criar um fork:

1. Acessar o repositório desejado.
2. Clicar em **Fork**.
3. Confirmar a criação da cópia na própria conta.
