## Como mostrar a branch do git no terminal do linux

- abra o arquivo .bashrc usando seu editor de textos preferido (vim, nano, gedit, mousepad) e procure pela expressão "PS1", que é relativa ao terminal e está logo abaixo da linha:
`if [ "$color_prompt" = yes ]; then`

Aqui no Debian (v.11), a linha PS1, está assim:
`PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '`

Adicione a expressão `__git_ps1 " (%s)"` antes de `\$`. 

Ficando assim:

``` bash
if [ "$color_prompt" = yes ]; then
    #PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]$(__git_ps1 " (%s)")\$ '
```

Salve o arquivo com as novas alterações. Recarregue as configurações do `.bashrc` com o comando: `source ~/.bashrc`

Antes:
`rrodrigues@debian:~/projeto-git$`

Depois: 
`rrodrigues@debian:~/projeto-git (main)$`

Referência:
[1] - https://sempreupdate.com.br/como-mostrar-a-branch-do-git-no-bash-no-linux 
