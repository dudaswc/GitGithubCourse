## Módulo 4 — Repositórios Remotos

### Criando um repositório no GitHub

Para armazenar e compartilhar projetos na nuvem, podemos criar um repositório no GitHub.

Passos básicos:

1. Acessar sua conta no GitHub.
2. Clicar em **New repository**.
3. Definir o nome do repositório.
4. Escolher se ele será **público** ou **privado**.
5. Clicar em **Create repository**.

Após a criação, o GitHub fornecerá as instruções para conectar o repositório local.

---

### Criando e adicionando uma chave SSH

A chave SSH permite conectar seu computador ao GitHub de forma segura, sem precisar digitar usuário e senha sempre.

Gerar uma chave SSH:

```bash
ssh-keygen -t ed25519 -C "seuemail@email.com"
````

Após gerar a chave, copiar o conteúdo da chave pública:

```bash
cat ~/.ssh/id_ed25519.pub
```

Depois:

1. Ir em **Settings** no GitHub
2. Acessar **SSH and GPG keys**
3. Clicar em **New SSH key**
4. Colar a chave copiada

---

### Ligando um repositório local a um remoto

Para conectar um repositório local ao GitHub:

```bash
git remote add origin URL_DO_REPOSITORIO
```

Verificar se o repositório foi conectado:

```bash
git remote -v
```

Enviar os arquivos para o GitHub:

```bash
git push -u origin main
```

---

### Clonando repositórios remotos

Clonar significa **baixar um repositório do GitHub para o computador**.

```bash
git clone URL_DO_REPOSITORIO
```

Esse comando cria uma cópia completa do projeto na sua máquina.

---

### Fazendo fork de um projeto

O **fork** é uma cópia de um repositório de outra pessoa para sua conta no GitHub.

Ele é muito utilizado em **projetos open source**, permitindo que você:

* faça modificações no código
* experimente melhorias
* envie contribuições para o projeto original

Para fazer um fork:

1. Acessar o repositório desejado no GitHub
2. Clicar no botão **Fork**
3. O projeto será copiado para sua conta

