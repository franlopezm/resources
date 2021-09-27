# Some GIT commands
---

## Crear y clonar proyectos

| Comando | Descripción |
| ------- | ----------- |
| `git init` | Inicializa git en un repositorio local |
| `git clone [https o ssh][url]` | Crea una copia local de un repositorio remoto |

## Básico

| Comando | Descripción |
| ------- | ----------- |
| `git status` | Comprueba si existen cambios en el repositorio actual |
| `git add [file-name]` | Añade un archivo nuevo o con cambios al stage |
| `git add -A` | Añade todos los archivos nuevos o con cambios al stage |
| `git reset [file-name]` | Retirar del stage un archivo añadido |
| `git commit -m "[commit message]"` | Confirmar los cambios con un mensaje |
| `git commit --amend -m "[commit message]"` | Cambia el mensaje del último commit realizado |
| `git rm -r [file-name]` | Elimina un archivo o carpeta |
| `git mv [file-nameA] [file-nameB]` | Mueve o cambia el nombre de un archivo de A a B |
| `git reset --hard [commit-hash]` | Vuelve a un commit especifico volviendo a dejar el repositorio como estaba en ese commit |
| `git reset --soft [commit-hash]` | Vuelve a un commit especifico y deja el stage como estaba en el commit especificado |

## Branch & Merger

| Comando | Descripción |
| ------- | ----------- |
| `git branch` | Lista las ramas, el asterísco indica la rama actual |
| `git branch -a` | Lista todas las ramas locales y remotas |
| `git fetch` | Actualiza la lista de ramas locales con las remotas |
| `git branch [branch name]` | Crea una nueva rama |
| `git branch -d [branch name]` | Elimina una rama |
| `git push origin --delete [branch name]` | Elimina una rama remota |
| `git checkout -b [branch name]` | Crea una nueva rama y cambia a ella |
| `git checkout -b [branch name] origin/[branch name]` | Clona una rama remota y cambia a ella |
| `git branch -m [old branch name] [new branch name]` | Renombra una rama local |
| `git checkout [branch name]` | Cambia a una rama existente |
| `git checkout -` | Cambia a la última rama |
| `git checkout -- [file-name.txt]` | Descarta los cambios para un archivo |
| `git merge [branch name]` | Unión de una rama dentro de la rama en la que nos encontramos |
| `git merge [source branch] [target branch]` | Unión de una rama dentro de otra rama destino |
| `git stash` | Guardar cambios realizados en el código y retomar la última versión o commit almacenado |
| `git stash list` | Listar todos los stash ejecutados |
| `git stash show -p [stash@{NUM}]` | Ver los cambios a recuperar de un stash |
| `git stash apply [stash@{NUM}]` | Aplicar los cambios del stash que queremos recuperar |
| `git stash clear` | Eliminar por completo los stash almacenados |
| `git stash drop [stash@{NUM}]` | Elimina el stash indicado |


## Actualizar proyectos

| Comando | Descripción |
| ------- | ----------- |
| `git push origin [branch name]` | Subir una rama al repositorio remoto |
| `git push -u origin [branch name]` | Subir los cambios a una rama del repositorio remoto |
| `git push -f origin [branch name]` | Fuerza la subida de cambios al repositorio remoto especificado |
| `git push` | Subir los cambios de la rama en la que nos encontramos al repositorio remoto |
| `git push origin --delete [branch name]` | Eliminar una rama remota |
| `git pull` | Actualizar la rama en la que nos encontramos en el repositorio local con los nuevos commit del repositorio remoto |
| `git pull origin [branch name]` | Actualizar el repositorio local con los cambios de la rama indicada en el repositorio remoto |
| `git remote add origin [https o ssh][url]` | Vincula el repositorio local con un repositorio remoto |
| `git remote set-url origin [ssh][url]` | Establecer la rama de origin en una rama por SSH |
| `git remote -v` | Listar las urls remotas y sus nombres |


## Tagging
Tag specific points in a repository's history as being important. Typically, people use this **functionality to mark release points** (v1.0, v2.0, and so on).

| Command | Description |
| ------- | ----------- |
| `git tag (--list or -l)` | Listing tags |
| `git tag -l "<tag name + pattern></tag>"` | Listing tags that match a particular pattern |
| `git tag -a <tag name> -m "<tagging message>"` | Create annotated tags, are stored as full objects in the Git database |
| `git tag <tag name>` | Create lightweight tags, it's just a pointer to a specific commit |
| `git tag -a <tag name> <commit checksum>` | Create a tag from a past commit |
| `git push origin <tag name>` | Transfer a specific tag to remote servers |
| `git push origin --tags` | Transfer all local tags to remote servers |
| `git tag -d <tag name>` | Delete a tag on local repository |
| `git push origin --delete <tag name>` | Delete a tag from remote servers |
| `git push <remote> :refs/tags/<tag name>` | Delete a tag from remote servers, when your tag may have the same name as your branch |


## Histórico y comparar

| Comando | Descripción |
| ------- | ----------- |
| `git log` | Ver el historial completo |
| `git log --summary` | Ver los detalles de los commit |
| `git log --oneline` | Ver los detalles de los commit resumidos |
| `git diff [source branch] [target branch]` | Vista previa de los cambios antes de realizar un merge |
| `git reflog` | Ver el historial completo, incluyendo incluso los cambios revertidos |

## Configuración

| Comando | Descripción |
| ------- | ----------- |
| `git config [--global, --local] user.name [nombre_usuario]` | Nombre mostrado en los commit, configurado globalmente o localmente |
| `git config [--global, --local] user.email [email_usuario]` | Email mostrado en los commit, configurado globalmente o localmente |

## Alias

| Comando | Descripción |
| ------- | ----------- |
| `git config --global alias.[nombre_alias] [comandos_git]` | Crea un alias para los comando indicados, se usa con _git[nombre_alias_] |


## Tools online
- [Git Command Explorer](https://gitexplorer.com)
