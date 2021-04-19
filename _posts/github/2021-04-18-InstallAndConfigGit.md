---
layout: post
title: Instalando e configurando a ferramenta Git.
excerpt: "Como instalar e configurar a ferramenta de controle de versão Git."
modified: 18/04/2021, 21:08:10
tags: [git, teminal, controle de versão, tutorial, dicas]
comments: false
category: blog
---

Após vários _backups_ do seus projetos sempre que você decide modificar o código mas não quer perder a versão antiga do seu código, você se deu conta que precisa de uma ferramenta que lhe ajude no controle de versão de código e após umas pesquisas você encontrou o Git.<br>
O Git é uma ferramenta para controle de versão usada mundialmente e neste artigo vamos mostrar a instalação e configuração em um sistema operacional Ubunto.<br>
Para dicas de como instalar em outras distribuições Linux e/ou outros sistemas operacionais acesse: <a href="https://git-scm.com/downloads" target="_blank"><u>Git-SCM</u></a>.


Instale o Git com o comando:
```shell
$ sudo apt-get install git
```

Após a instalação do Git, a primeira ação que você de tomar é a configuração do Git. Com isso iremos definir nome de usuário, e-mail e editor de preferência.<br>
O Git guarda as suas informações em 3 lugares:

- git config do sistema como um todo.
- git config do usuário.
- git config do projeto específico daquele repositório.

Como vamos definir informações para todos os repositórios deste usuário atual, vamos utilizar o _config_ do usuário, o `global`.


Para definir o nome de usuário:
```shell
$ git config --global user.name "meu nome de usuário"
```
Se ocorreu algum erro irá aparecer no terminal, caso contrário não irá aparecer nada.

 Para definir o seu email:
```shell
$ git config --global user.email "meu-email@exemplo.com" 
```

Para definir o seu editor de texto:
```shell 
$ git config --global core.editor vim 
```
> Neste exemplo usamos o vim.

Para ver qual valor está configurado em um dos parâmetros basta digitar `git config parametro`. Por exemplo:
```shell
$ git config user.name
meu nome de usuário
```

Para listar as identificações atribuídas até então:
```shell
$ git config --list
```

_lista exemplo_:
```shell
user.email=meu-email@exemplo.com
user.name=meu nome de usuário
core.editor=vim
```

<p>
    <img src="../../images/git-logo.png" alt="Git" title="Git"/>
</p>