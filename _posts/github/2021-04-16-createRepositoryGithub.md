---
layout: post
title: Criando e vinculando seu primeiro repositório no GitHub.
excerpt: "Como ."
modified: 16/04/2021, 23:30:10
tags: [github, teminal, repositorio, tutorial]
comments: false
category: blog
---

Você iniciou no universo da programação e decidiu usar o [GitHub](https://github.com/) para ser sua plataforma de controle de versão ou simplesmente para armazenar seus códigos na nuvem, mas ainda não sabe como criar e vincular seu repositório à sua pasta com seu projeto em seu computador. Pois nesse artigo vamos lhe ensinar como fazer isso você irá ver que é algo super simples.

- [Criar repositório](#criar-repositório)
- [Vincular repositório](#vincular-repositório)
  
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
5 $ git branch -M main
6 $ git remote add origin https://github.com/nome-de-usuario/nome-do-repositorio.git
7 $ git push -u origin main
```
- Linha 1: cria um arquivo README.md com o texto "nome-do-repositório";
- Linha 2: inicializa o repositório git na pasta atual;
- Linha 3: adiciona TODOS os arquivos para _tracking_;
- Linha 4: adiciona o _commit_ "primeiro commit" em todos os arquivos em _tracking_;
- Linha 5: cria uma _branch_ com o nome "main";
- Linha 6: liga remotamente seu projeto em seu computador ao repositório no GitHub;
- Linha 7: sobe os arquivos do seu computador para o seu repositório no GitHub. Insira nome de usuário e senha quando for pedido.


  <p>
    Note que após feito isso pela primeira vez você apenas irá precisar executar os comandos 3, 4 e 7 quando for subir novos arquivos para seu repositório.
  </p>
  
