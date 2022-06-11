# Git

Git es un sistema de control de versiones, resgistra todo el historial de cambios de un proyecto.

## Repositorio

Es todo proyecto que esta siendo seguido por git. Tiene un historial de git en el que estan registrados sus cambios.

### Repositorio local

Este repositorio esta por defecto en el ordenador.

### Repositorio remoto (nube)

Son versiones de un proyecto que estan hospedadas en Internet o en una red social (github.com, gitlab.com, etc)

## Branch

Hace posible desarrollar nuevas funciones de un proyecto sin obstaculizar el desarrollo de la rama principal.

### Branch Main.

Es la rama principal (master)

### Branch

Es una rama de desarrollo donde se crean cambios para despues ser evaluados y agregados a la rama principal _Main_

![](https://i.stack.imgur.com/83JeN.png)

## Commit

Es cada uno de los cambios registrados en el historial de git.

### Mensaje en un Commit

```
    type (theme) : ¿qué se esta cambiando y para qué?
    1 - 2 parrafos.
```

_Ejemplo_

```
    docs(git): creando un documento sobre git y sus comandos

    Añadiendo información sobre qué es git.
    Describiendo para qué sirve cada elemento y comando en git.
```

## Comandos de git

### git status

Muestra el estado actual del repositorio.

```sh
learn-x-in-y-minutes [kna-git-notes] git status
On branch kna-git-notes
Your branch is up to date with 'origin/kna-git-notes'.

nothing to commit, working tree clean

```

### git add

Agrega archivos o agrega un commit.

```sh
learn-x-in-y-minutes [kna-git-notes] git add git/git-commands.md
learn-x-in-y-minutes [kna-git-notes] git status
On branch kna-git-notes
Your branch is up to date with 'origin/kna-git-notes'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
```

### git checkout

Cambia de rama.

```
learn-x-in-y-minutes [kna-git-notes] git checkout main
learn-x-in-y-minutes [main]
learn-x-in-y-minutes [main] git checkout kna-git-notes
learn-x-in-y-minutes [kna-git-notes]
```

### git commit

Compromete los cambios y se debe agregar un mensaje como estos cambios.

```
learn-x-in-y-minutes [kna-git-notes] ⚡  git commit
[kna-git-notes c241d41] docs(git): add more information about git
 1 file changed, 22 insertions(+)
```
