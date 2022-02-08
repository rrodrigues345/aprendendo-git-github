Olá! 

Neste projeto, a Rafa Ballerini ensina a utilizar o Git. Acompanhe pelo vídeo abaixo:

[![COMO USAR GIT E GITHUB NA PRÁTICA! - desde o primeiro commit até o pull request! 2/2](https://img.youtube.com/vi/UBAX-13g8OM/0.jpg)](https://www.youtube.com/watch?v=UBAX-13g8OM)

##

## Introdução

GitHub é uma plataforma de hospedagem de código para controle de versões e colaboração, possibilitando trabalho em conjunto em projetos de qualquer lugar do mundo. 

### Repositório

De forma geral, repositórios são utilizados para organizar um único projeto. Podem conter pastas e arquivos, imagens, vídeos, planilhas e tudo o mais necessário a seu projeto. Frequentemente, os repositórios incluem um arquivo `README`, um tipo de arquivo que contém informação sobre o seu projeto. 

### Iniciando um projeto

#### Iniciando o Git no Terminal

- crie uma pasta no seu computador com o nome do projeto: `aprendendo-git-github`.
- comece a criar os arquivos dentro de sua pasta.
    - vc pode abrir a pasta direto pelo Visual Studio Code ou outra IDE de sua preferência.
- inicie o git: 
    - `git init`
- adicione os arquivos criados: `git add .`
- veja o status do git: `git status`

``` bash
rrodrigues@debian:~/projetos/aprendendo-git-github (master)$ git status 

On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   Projeto.md
	new file:   Readme.md
	new file:   img/criando-repositorio.png
	new file:   img/link-do-repositorio.png

```

- faça seu primeiro commit: `git commit -m "Primeiro commit do projeto!"`

``` bash
rrodrigues@debian:~/projetos/aprendendo-git-github (master)$ git commit -m "Primeiro commit!"

[master (root-commit) 2d40d94] Primeiro commit!
 4 files changed, 57 insertions(+)
 create mode 100644 Projeto.md
 create mode 100644 Readme.md
 create mode 100644 img/criando-repositorio.png
 create mode 100644 img/link-do-repositorio.png

```

- vamos trocar o nome da branch de **master** para **main**: `git branch -M "main"`

``` bash
rrodrigues@dell:~/projetos/aprendendo-git-github (main)$ git status 
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")
```
Veja que o arquivo Readme.md está indicado como: "modified:   Readme.md" pois estou editando este arquivo durante o commit.

#### Criando o projeto no GitHub

- No github, na sua conta de usuário, crie um projeto. Vá em **Novo** --> **Repositório** e crie a pasta **aprendendo-git-github**. Marque a opção "Público" e clique em "Criar repositório".

![Criando um repositório no GitHub](./img/criando-repositorio.png)

Na página de instruções que abrir, copie o link do seu repositório do github:

![Link do repositório no GitHub](./img/link-do-repositorio.png)

O meu link aqui, ficou assim:
`https://github.com/rrodrigues345/aprendendo-git-github.git`

#### Conectando Git & GitHub =)

De posse do link do repositório no GitHub, vamos conectar o git com o repositório do github:

git remote add origin https://github.com/rrodrigues345/aprendendo-git-github.git

Feito isso, podemos enviar os arquivos para nosso repositório, usando o comando: `git push -u origin main`

``` bash
rrodrigues@debian:~/projetos/aprendendo-git-github (main)$ git push -u origin main 
Username for 'https://github.com': rrodrigues345
Password for 'https://rrodrigues345@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 80.73 KiB | 10.09 MiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/rrodrigues345/aprendendo-git-github.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
rrodrigues@debian:~/projetos/aprendendo-git-github (main)$ 
```










## Referências

[1] - https://docs.github.com/en/get-started/quickstart/hello-world
[2] - Ballerini, Rafaella. 2021. Como usar Git e GitHub na prática: do primeiro commit até o pull request. Disponível em: https://www.youtube.com/watch?v=UBAX-13g8OM.