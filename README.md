![git_2](https://user-images.githubusercontent.com/23192401/62431296-e6f69400-b6eb-11e9-89cc-b4e54d2dd4d6.jpg)

# ****************** COMANDOS GIT - Geo ******************

## Configuración Básica GIT

Configurar Nombre que salen en los commits
```ssh
```
Configurar Email
```ssh	
	git config --global user.email dasdo1@gmail.com
```
Marco de colores para los comando
```ssh
	git config --global color.ui true
```
Listar configuración
```ssh
	git config --list
```

## Iniciando repositorio

Iniciamos GIT en la carpeta donde esta el proyecto
```ssh
	*$ git init
```
Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Añadimos todos los archivos para el commit
```ssh
	*$ git add .
```
Hacemos el primer commit
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
	
	Editar el mensaje de un commit:
	
	git commit --amend -m “feat: Revised commit message”
```
subimos al repositorio
```ssh
	git push origin master
```

## GIT CLONE *****


Clonamos el repositorio de github o bitbucket
```ssh
	git clone <url>
```
Clonamos el repositorio de github o bitbucket ?????
```ssh
	git clone <url> git-demo
```

## GIT ADD *****


Añadimos todos los archivos para el commit
```ssh
	git add .
```
Añadimos el archivo para el commit
```ssh
	git add <archivo>
```
Añadimos todos los archivos para el commit omitiendo los nuevos
```ssh
	git add --all 
```
Añadimos todos los archivos con la extensión especificada
```ssh
	git add *.txt
```
Añadimos todos los archivos dentro de un directorio y de una extensión especifica
```ssh
	git add docs/*.txt
```
Añadimos todos los archivos dentro de un directorios
```ssh
	git add docs/
```
## GIT COMMIT *****

Cargar en el HEAD los cambios realizados
```ssh
	git commit -m "Texto que identifique por que se hizo el commit"
```
Agregar y Cargar en el HEAD los cambios realizados
```ssh
	git commit -a -m "Texto que identifique por que se hizo el commit"
```
De haber conflictos los muestra
```ssh
	git commit -a 
```
Modificación del mensaje del commit de Git más reciente.
```ssh
	git commit --amend
	git commit --amend -m "an updated commit message"
	git commit --amend --no-edit
```
## GIT PUSH *****

Subimos al repositorio
```ssh
	*$ git push <origien> <branch>
    
    Ejemplo:
    
    $ git push -u origin master
    
```
Subimos un tag
```ssh
	git push --tags
```
## GIT LOG *****

Muestra los logs de los commits
```ssh
	git log
```
Muestras los cambios en los commits
```ssh
	git log --oneline --stat
```
Muestra graficos de los commits
```ssh
	git log --oneline --graph
```
Muestra las diferencias introducidas en cada confirmación
```ssh
	git log -p
	git log -p -2
```
## GIT DIFF *****

Muestra los cambios realizados a un archivo
```ssh
	git diff
	git diff --staged
    
    Ejemplo:
    $ git diff index.html
```
## GIT HEAD

Saca un archivo del commit
```ssh
	git reset HEAD <archivo>
```
Devuelve el ultimo commit que se hizo y pone los cambios en staging
```ssh
	git reset --soft HEAD^
```
Devuelve el ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^
```
Devuelve los 2 ultimo commit y todos los cambios
```ssh
	git reset --hard HEAD^^
```
Rollback merge/commit
```ssh
	git log
	git reset --hard <commit_sha>
```
## GIT REMOTE *************

Agregar repositorio remoto
```ssh
	*$ git remote add origin <url>
```
Cambiar de remote
```ssh
	git remote set-url origin <url>
```
Remover repositorio
```ssh
	git remote rm <name/origin>
```
Muestra lista repositorios
```ssh
	git remote -v
```
Muestra los branches remotos
```ssh	
	git remote show origin
```
Limpiar todos los branches eliminados
```ssh
	git remote prune origin 
```
## GIT BRANCH ********** $$$$ ************

Crea un branch
```ssh
	git branch <nameBranch>
```
Lista los branches (Ramas o versiones alternas)
```ssh
	git branch
```
Comando -d elimina el branch y lo une al master
```ssh
	git branch -d <nameBranch>
```
Elimina sin preguntar
```ssh
	git branch -D <nameBranch>
```
Cambiar de branch o version ****$$$
```ssh
	git checkout <nameBranch/tagname>
    
    Ejemplo:
    
    $ git checkout login
```
## GIT TAG

Muestra una lista de todos los tags
```ssh
	git tag
```
Crea un nuevo tags
```ssh
	git tag -a <verison> - m "esta es la versión x"
```
Tags commans
```ssh
	Listado de etiquetas:
	git tag
	
	Cambio de etiquetas:
	git checkout v1.4
	
	Eliminación de etiquetas:
	git tag -d v1
```


## GIT REBASE

Los rebase se usan cuando trabajamos con branches esto hace que los branches se pongan al día con el master sin afectar al mismo

Une el branch actual con el mastar, esto no se puede ver como un merge
```ssh
	git rebase
```
Cuando se produce un conflicto no das las siguientes opciones:

cuando resolvemos los conflictos --continue continua la secuencia del rebase donde se pauso
```ssh	
	git rebase --continue 
```
Omite el conflicto y sigue su camino
```ssh
	git rebase --skip
```
Devuelve todo al principio del rebase
```ssh
	git reabse --abort
```
Para hacer un rebase a un branch en especifico
```ssh	
	git rebase <nameBranch>
```
## GIT DIFF

El comando Diff se usa para vizualisar las diferencias entre objetos (ramas, commits, archivos, entre otros)

Muestra los archivos que no se encuentran en el repositorio en la rama actual
```ssh
	git diff
```
Muestra las diferencias entre commits
```ssh
	git diff 1234abc 6789def    #antiguo   nuevo
```
Muestra las diferencias de archivos de la "staged area"
```ssh
	git diff --staged
```
Muestra las diferencias entre ramas
```ssh
	git diff rama1 rama2
```
Muestra las diferencias en un archivo especifico
```ssh
	git diff miarchivo.txt
```
Muestra las archivos con cambios en un directorio
```ssh
	git diff documentation
```
## OTROS COMANDOS

Lista un estado actual del repositorio con lista de archivos modificados o agregados
```ssh
	*$ git status
```
Quita del HEAD un archivo y le pone el estado de no trabajado
```ssh
	*$ git checkout -- <file>
```
Crea un branch en base a uno online
```ssh
	git checkout -b newlocalbranchname origin/branch-name
```
Busca los cambios nuevos y actualiza el repositorio
```ssh
	git pull origin <nameBranch>
```
Cambiar de branch
```ssh
	git checkout <nameBranch/tagname>
```
Une el branch actual con el especificado
```ssh
	git merge <nameBranch>
```
Verifica cambios en el repositorio online con el local
```ssh
	git fetch
```
Borrar un archivo del repositorio
```ssh
	git rm <archivo> 
```

## Fork

Descargar remote de un fork
```
	git remote add upstream <url>
```

Merge con master de un fork
```
	git fetch upstream
	git merge upstream/master
```

## Adicional - Geo

Crear un archivo “.gitignore” en el cual colocamos los directorios o archivos que deseamos omitir o ignorar. Añadir el archivo con:
```
    .gitignore
    
    $ git add .gitignore

```

# INFORMACIÓN WEB
## Recuperar un archivo o todo el repositorio a una versión anterior

* **https://victorhckinthefreeworld.com/2016/07/28/git-recuperar-un-archivo-o-todo-el-repositorio-a-una-version-anterior/**

```ssh
Restaurar a una versión antigua en el directorio de trabajo:

git checkout 55df4c2 prueba.txt

git add prueba.txt
git commit -m "texto de commit"

Llevar todos los archivos del repositorio a un punto predeterminado:

git checkout 55df4c2

Seguir este consejo:

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

```

# Config File

```
movil-cliente/.git/config


[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
[remote "origin"]
	url = http://git.kubxycorp.com/aplicaciones/entodositio.com/movil/movil-cliente.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master
[branch "desarrollo"]
	remote = origin
	merge = refs/heads/desarrollo

```

## GIT STASH

```
# Git Pull While Ignoring Local Changes

If on the other hand you want to keep the local modifications somehow, you'd use stash to hide them away before pulling, then reapply them afterwards:

git stash
git pull
git stash pop

git merge <rama>
git log --oneline --decorate --all --graph // --color



Cómo guardar el trabajo en un stash.
git stash
git stash save "mensaje"

Cómo volver a aplicar los cambios de un stash (Aplica los cambio y elimina el stash).
git stash pop
git stash pop stash@{2}

Aplicar los cambios en el código en el que estás trabajando y conservarlos en tu stash.
git stash apply

Cómo gestionar varios stashes
git stash list

Para contextualizar, es recomendable comentar los stashes con una descripción.
git stash save "mensaje"

Cómo ver las diferencias en un stash
git stash show
git stash show -p

Stashes parciales (Revisar tabla en url).
git stash -p
https://www.atlassian.com/es/git/tutorials/saving-changes/git-stash

Cómo limpiar el stash.
git stash drop stash@{1}

También tienes la opción de eliminar todos los stashes.
git stash clear

```

## Sincroniza tu rama maestra con la del repositorio original
* **https://www.freecodecamp.org/espanol/news/como-hacer-tu-primer-pull-request-en-github/**
```
$ git branch
$ git checkout master

Agrega el repositorio original como un repositorio upstream.

$ git remote add upstream [HTTPS]

Busca (fetch) el repositorio.

$ git fetch upstream

Fusionala.

$ git merge upstream/master

Envía (push) los cambios a GitHub

$ git push origin master
$ git remote rm [Nombre del Repositorio Remoto]

```

# REPOSITORY

```
…or create a new repository on the command line
echo "# entodositio-conductores" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/repository.git
git push -u origin main
                
…or push an existing repository from the command line
git remote add origin https://github.com/repository.git
git branch -M main
git push -u origin main
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.

Ver url repositorio remoto:

git remote -v

```

# Conventional Commits

* **http://conventionalcommits.org/en/v1.0.0/**

```
The commit message should be structured as follows:

<type>[optional scope]: <description>

[optional body]

[optional footer(s)]

The commit contains the following structural elements, to communicate intent to the consumers of your library:

1. fix: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in semantic versioning).
2. feat: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in semantic versioning).
3. BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in semantic versioning). A BREAKING CHANGE can be part of commits of any type.
4. types other than fix: and feat: are allowed, for example @commitlint/config-conventional (based on the the Angular convention) recommends build:, chore:, ci:, docs:, style:, refactor:, perf:, test:, and others.
5. footers other than BREAKING CHANGE: <description> may be provided and follow a convention similar to git trailer format.

Additional types are not mandated by the Conventional Commits specification, and have no implicit effect in semantic versioning.

Examples

git commit -m 

fix: correct minor typos in code see the issue for details on typos fixed.
feat: allow provided config object to extend other configs
docs: correct spelling of CHANGELOG

```

## ELIMINAR RAMAS LOCALES Y REMOTAS
```
Para eliminar una rama de nuestro repositorio local ejecutaremos el siguiente comando:


$ git branch -d nombre_rama

En el caso de que esa rama contenga trabajos sin fusionar, el comando anterior nos devolverá el siguiente error:


error: The branch 'nombre-rama' is not an ancestor of your current HEAD.
If you are sure you want to delete it, run 'git branch -D nombre-rama'.

Si aún así queremos eliminar esa rama, se puede forzar el borrado de la siguiente manera:


$ git branch -D nombre-rama

En el caso de querer eliminar una rama del repositorio remoto, la sintaxis será la siguiente:


$ git push origin :nombre-rama

Y de esta forma, desaparecerá la rama nombre-rama del servidor.
```

## Generar una nueva clave SSH y agregarla al ssh-agent

* **https://docs.github.com/es/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent**
* **https://jhooq.com/github-permission-denied-publickey/**

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
cat /c/Users/name-user/.ssh/id_rsa.pub

Agregar la clave en /Setting/SSH and GPG keys

```


