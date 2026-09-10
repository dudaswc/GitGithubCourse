# Módulo 2 — Configurando o Git

## Instalando o Git

O Git precisa estar instalado no computador para que seus comandos possam ser utilizados no terminal.

Passos básicos:

1. Acessar o [site oficial do Git](https://git-scm.com).
2. Baixar a versão compatível com o sistema operacional.
3. Executar o instalador.
4. Verificar a instalação com:

```bash
git --version
```

## Configuração inicial

Antes de criar commits, é necessário informar ao Git o nome e o e-mail que serão associados ao histórico:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
```

Para conferir as configurações cadastradas:

```bash
git config --list
```

A opção `--global` aplica os dados a todos os repositórios do usuário no computador.
