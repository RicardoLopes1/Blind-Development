---
layout: post
title: Criando e vinculando seu primeiro repositório no GitHub.
excerpt: "Como criar e vincular um repositório no GitHub à uma pasta em seu computador."
modified: 18/04/2021, 19:45:10
tags: [github, teminal, repositorio, tutorial]
comments: false
category: blog
---

Você iniciou no universo da programação e decidiu usar o [GitHub](https://github.com/) para ser sua plataforma de controle de versão ou simplesmente para armazenar seus códigos na nuvem, mas ainda não sabe como criar e vincular seu repositório à sua pasta com seu projeto em seu computador. Pois nesse artigo vamos lhe ensinar como fazer isso e você irá ver que é algo super simples.<br>
Primeiro passo é instalar e configurar a ferramenta Git em seu computador, caso não tenha feito isso ainda <a href="2021-04-18-InstallAndConfigGit.md" target="_blank"><u>clique aqui</u></a>. Com a ferramenta Git instalada e configurada vamos para os próximos passos.

- [Criar repositório](#criar-repositório)
- [Vincular repositório](#vincular-repositório)
- [Pulo do gato](#pulo-do-gato)
  
## Criar Repositório

Primeiro passo é criar uma conta no [GitHub](https://github.com/) e acessar sua conta. <br>
Após entrar em sua conta vá em seus repositórios e clique no botão "novo".
  <p>
    <img src="../../images/btn-new-repository.jpg" alt="Botão novo" title="Botão Novo"/>
  </p>

Após clicar no botão "Novo" escolha um nome para seu repositório e uma descrição (opcional).<br>
Após a descrição selecione se seu repositório será público ou privado (neste caso vamos selecionar público).<br>
Agora clique no botão "Criar repositório".
  <p>
    <img src="../../images/btn-ok-repository.png" alt="Botão Criar repositório" title="Criar repositório"/>
  </p>

  E pronto! Repositório criado.

## Vincular Repositório

Com o repositório criado, abra seu terminal e navegue até a pasta com o seu projeto que deseja vincular e digite os seguintes comandos:<br>

``` shell
1 $ echo "# nome-do-repositório" >> README.md 
2 $ git init
3 $ git add .
4 $ git commit -m "primeiro commit"
5 $ git remote add origin https://github.com/nome-de-usuario/nome-do-repositorio.git
6 $ git push -u origin master
```
- Linha 1: cria um arquivo README.md com o texto "nome-do-repositório";
- Linha 2: inicializa o repositório git na pasta atual;
- Linha 3: adiciona __TODOS__ os arquivos para _tracking_;
- Linha 4: adiciona o _commit_ "primeiro commit" em todos os arquivos em _tracking_;
- Linha 5: liga remotamente seu projeto em seu computador ao repositório no GitHub;
- Linha 6: sobe os arquivos do seu computador para o seu repositório no GitHub. Insira nome de usuário e senha quando for pedido.


  <p>
    Note que após feito isso pela primeira vez você apenas irá precisar executar os comandos 3, 4 e 7 quando for subir novos arquivos para seu repositório.
  </p>

## Pulo do gato

Agora iremos mostrar uma forma mais simples de ter seu repositório do GitHub vinculado à um projeto em seu computador.<br>
Após criar seu repositório no GitHub, copie a _URL_ do seu repositóio, abra seu terminal em uma pasta que deseja ter esse repositório e digite o comando para clonar:
```shell
1 $ git clone https://URL-DO-REPOSITORIO/
```
Esse comando irá criar um clone do seu repositório em seu computador, ou seja, uma pasta já vinculada. Agora basta por todo o código fonte do seu projeto nessa pasta e dar os comandos para fazer o _tracking_, o _commit_ e subir os códigos.
```shell
1 $ git add .
2 $ git commit -m "primeiro commit"
3 $ git push
``` 

<p>
    <img src="../../images/github-logo.png" alt="GitHub" title="GitHub"/>
  </p>

  
