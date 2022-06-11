# Git

Git es un sistema de control de versiones, resgistra todo el historial de cambios de un proyecto.

## Repositorio

Es todo proyecto que esta siendo seguido por git. Tiene un historial de git en el que estan registrados sus cambios.

### Repositorio Local

Este repositorio esta por defecto en el ordenador.

### Repositorio Remoto

Son versiones de un proyecto que estan hospedadas en Internet o en una red social (github.com, gitlab.com, etc)

![](https://i.morioh.com/210405/3c59afec.webp)

## Branch

Hace posible desarrollar nuevas funciones de un proyecto sin obstaculizar el desarrollo de la rama principal.

### Branch Main

Es la rama principal, se puede llamar también Master.

### Branch Secundary

Es una rama de desarrollo donde se crean cambios, si se desea se mandan a ser evaluados para despues poder ser agregados a la rama principal _Main_

![](https://i.stack.imgur.com/83JeN.png)

## Commit

Es cada uno de los cambios registrados en el historial de git.

Existen diversas maneras de hacer un commit. Un ejemplo de ellas seria:

```sh
    type (theme) : ¿qué se esta cambiando y para qué?

    1 - 2 parrafos.
```

_Ejemplo_

```sh
    docs(git): creando un documento sobre git y sus comandos

    Añadiendo información sobre qué es git.
    Describiendo para qué sirve cada elemento y comando en git.
```

## Comandos de `git`

### `git clone`

Clona un repositorio ya existente.

```sh
github.com  git clone git@github.com:katherine-na/learn-x-in-y-minutes.git
Cloning into 'learn-x-in-y-minutes'...
remote: Enumerating objects: 88, done.
remote: Counting objects: 100% (88/88), done.
remote: Compressing objects: 100% (86/86), done.
remote: Total 88 (delta 17), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (88/88), 293.70 KiB | 1.72 MiB/s, done.
Resolving deltas: 100% (17/17), done.
github.com  ls
git-play              introduction-to-linux learn-x-in-y-minutes

```

### `git branch`

Son ramas donde se desarrolla el proyecto.  
Puede visualizar las ramas existentes, por ejemplo.

```sh
learn-x-in-y-minutes [main] git branch
kna-git-notes
kna-update
[main]
(END)
```

Puede crear una rama, por ejemplo:

```sh
learn-x-in-y-minutes [main] git branch kna-linux-notes
learn-x-in-y-minutes [main] git checkout kna-linux-notes
Switched to branch 'kna-linux-notes'
```

Puede eliminar una rama, por ejemplo.

```
learn-x-in-y-minutes [main]  git branch --delete kna-update
Deleted branch kna-update (was d119bbd).
```

### `git pull`

Actualiza la versión local de un repositorio desde otro remoto.

```sh
learn-x-in-y-minutes [main] git pull
remote: Enumerating objects: 2, done.
remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), done.
From github.com:katherine-na/learn-x-in-y-minutes
   919e96b..0b059f9  main       -> origin/main
Updating 919e96b..0b059f9
Fast-forward
 git/git-commands.md | 72 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 1 file changed, 72 insertions(+)
```

### `git push`

Carga el contenido del repositorio local a un repositorio remoto.

```sh
learn-x-in-y-minutes [kna-git-notes] git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 860 bytes | 860.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:katherine-na/learn-x-in-y-minutes.git
   c241d41..effcc19  kna-git-notes -> kna-git-notes
```

### `git status`

Muestra el estado actual del repositorio.

```sh
learn-x-in-y-minutes [kna-git-notes] git status
On branch kna-git-notes
Your branch is up to date with 'origin/kna-git-notes'.

nothing to commit, working tree clean

```

### `git log`

Es el historial de commits de un repositorio.

```sh
commit effcc19fa4e0f65c79bb282ebf9a046e9cb59b4b (HEAD -> kna-git-notes, origin/kna-git-notes)
Author: Katherine Negrete <katherine.negrete.aguilar@gmail.com>
Date:   Sat Jun 11 13:32:46 2022 -0500

    docs(git): added more information

    Add git commands and write information with examples.

commit c241d4105f87f6e59f35a2012dbed5adb1f1c874
Author: Katherine Negrete <katherine.negrete.aguilar@gmail.com>
Date:   Sat Jun 11 13:04:03 2022 -0500

    docs(git): add more information about git

    I wrote more information about the structure of git.
    I added an image to give an example.

commit 5653b9d5ff35eeed9f68ce264eb6167d5b107f79
Author: Katherine Negrete <katherine.negrete.aguilar@gmail.com>
Date:   Sat Jun 11 12:26:25 2022 -0500

    docs(git): creating a document about git

    Defining what git is and what it is for.
    Adding examples on how to write a commit.

```

### `git add`

Agrega archivos o agrega un commit.

```sh
learn-x-in-y-minutes [kna-git-notes] git add git/git-commands.md
learn-x-in-y-minutes [kna-git-notes] git status
On branch kna-git-notes
Your branch is up to date with 'origin/kna-git-notes'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
```

### `git checkout`

Cambia de rama.

```sh
learn-x-in-y-minutes [kna-git-notes] git checkout main
learn-x-in-y-minutes [main]
learn-x-in-y-minutes [main] git checkout kna-git-notes
learn-x-in-y-minutes [kna-git-notes]
```

### `git commit`

Compromete los cambios y se debe agregar un mensaje como estos cambios.

```sh
learn-x-in-y-minutes [kna-git-notes] ⚡  git commit
[kna-git-notes c241d41] docs(git): add more information about git
 1 file changed, 22 insertions(+)
```
