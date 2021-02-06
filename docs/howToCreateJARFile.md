> Created by [Ricardo Lopes](https://github.com/RicardoLopes1).

# Table of content - *Tabela de conteúdo*
- [English](#english);
- [Português](#português);


## English
How to create a Java executable file (.Jar) using the terminal.

We'll use an example file called HelloWorld.java. First compile all your files and move them to a directory of compiled classes, as in [example 1](#example-1) or [example 2](#example-2) (to compile all .java files).

#### example 1
``` java
$ javac HelloWorld.java
$ mkdir classFiles
$ mv HelloWorld.class classFiles
```

#### example 2
```java
$ javac *.java
$ mkdir classFiles
$ mv *.class classFiles
```

Now that we have all the files compiled, let's create our executable!

- Step 1:
  
  Create a manifest file in the same directory as your .class files (in this case, the directory is classFiles).

  Open the terminal in the ClassFiles directory and type:
  ```shell
  $ touch Manifest.txt
  ```

  Now open this file using a text editor (in this example, we'll use gedit).
  ```shell
  $ gedit Manifest.txt
  ```

  Insert the following text into the file and save. `HelloWorld` is the main class.
  ```txt
  Main-Class: HelloWorld
  ```

  **NOTE: the Manifest.txt file must end with a blank line. Otherwise, an error will occur.**

- Step 2:
  
  Still inside the classFiles directory, type the following command in the terminal:
  ```shell
  $ jar cfm app.jar Manifest.txt *.class
  ```

  An `app.jar` file will be created in that directory.

- Step 3:
  
  Run your program by typing the following command in the terminal:
  ```shell
  $ java -jar app.jar
  ```
---

## Português
Como criar um arquivo executável Java (.Jar) usando o terminal.

Usaremos um arquivo exemplo com o nome OlaMundo.java. Primeiro compile todos os seus arquivos e mova-os para um diretório de classes compiladas, como no [exemplo 1](#exemplo-1) ou [exemplo 2](#exemplo-2) (para compilar todos os arquivos .java).

#### exemplo 1
``` java
$ javac OlaMundo.java
$ mkdir arquivosClass
$ mv OlaMundo.class arquivosClass
```

#### exemplo 2
```java
$ javac *.java
$ mkdir arquivosClass
$ mv *.class arquivosClass
```

Agora que temos todos os arquivos já compilados, vamos criar nosso executável!

- Passo 1:
  
  Crie um arquivo de manifesto no mesmo diretório onde está seus arquivos .class (nesse caso, o diretório é o arquivosClass). 
  
  Abra o terminal no diretório arquivosClass e digite:
  ```shell
  $ touch Manifest.txt
  ```

  Agora abra esse arquivo usando um editor de texto (nesse exemplo usaremos o gedit).
  ```shell
  $ gedit Manifest.txt
  ```

  Insira o seguinte texto dentro do arquivo e salve. `OlaMundo` é a classe principal.
  ```txt
  Main-Class: OlaMundo
  ```

  **NOTA: o arquivo Manifest.txt deve terminar com uma linha em branco. Caso contrário, ocorrerá um erro.**

- Passo 2: 
  
  Ainda dentro do diretório arquivosClass digite o seguinte comando no terminal:
  ```shell
  $ jar cfm app.jar Manifest.txt *.class
  ```

  Um arquivo `app.jar` será criado nesse diretório.

- Passo 3:

  Para executar seu programa digite no terminal o seguinte comando:
  ```shell
  $ java -jar app.jar
  ```

  
