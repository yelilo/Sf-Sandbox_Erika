# Sf-Sandbox_Erika
## Instrucciones para crear un repositorio en github
1. Instala Git
2. Crea cuenta en github
3. Copia la URL del repositorio
4. Abre git bash en donde quieres que se almacene tu proyecto dentro de tu ordenador
5. Escribe dentro de la consola, quitando las llaves > git clone <Pega URL_Repositorio>

## Configura entorno local
- Revisa la configuracion actual agregando la siguiente linea en consola > git config --list
- Si no tiene tu nombre y correo, genera configuracion corriendo las siguientes lineas
    - > git config --global user.name "First Last"
    - > git config --global user.email "you@email.com"

### Configuracion de  **autocrlf**
No entiendo muy bien para que sirve pero cito el texto encontrado:
"_A continuación, configuramos core.autocrlf (autocrlf significa avance de línea de retorno de carro automático). Los diferentes sistemas manejan los finales de línea y los saltos de línea de manera diferente. Si abre un archivo creado en otro sistema operativo y no tiene esta opción de configuración establecida, Git pensará que realizó cambios en el archivo según la forma en que su sistema operativo maneja los finales de línea._". Thailhead Trabaja con el flujo de trabajo de github (2021).

Para usuarios de Windows, ingrese:

> git config --global core.autocrlf true

Para usuarios de Mac o Linux, ingrese:

>git config --global core.autocrlf input

## Creación de Rama
Con la configuración inicial generamos la Rama Maestra del repositorio, lo ideal es trabajar en distintas ramas si se tiene varios desarrollos involucrados para evitar que choquen y encontrar rupturas que puede aver entre desarrollos.

Escribe
> git branch

Puedes visualizar las ramas existentes

Genera una nueva rama con las siguientes lineas
1. > git branch _Nombre_de_la_rama_
2. > git checkout _Nombre_de_la_rama_

## Subir cambios a proyecto
1. Revisa si hay modificaciones en tu proyecto
    > git status

    Veras en la consola un codigo similar a este
    ~~~
    $ git status
    On branch NombreDeTuRama
    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
            modified:   README.md

    no changes added to commit (use "git add" and/or "git commit -a")
    ~~~

2. Añade tus cambios a un paquete de subida (arbol)
    > git add README.md

3. Revisa que se haya añadido tu archivo revisando el Status nuevamente como el paso 1
    ~~~
    $ git status
    On branch NombreDeTuRama
    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
            modified:   README.md
    ~~~

4. Crea nota con con cambios realizados

    > git commit -m "Detalle de los cambios a subir"

    ~~~
    $ git commit -m "Añade información de como integrar proyecto de salesforce a github, usando git"
    [NombreDeTuRama 8f70286] Añade información de como integrar proyecto de salesforce a github, usando git
    1 file changed, 31 insertions(+)
    ~~~

5. Revisa que tu Commit se haya documentado correctamente
    > git status
    ~~~
    $ git status
    On branch NombreDeTuRama
    nothing to commit, working tree clean
    ~~~

## Enviar cambios a repositorio remoto
1. Escribe la siguiente linea en consola para enviar tus cambios al servidor de github
    > git push -u origin NombreDeTuRama
    ~~~
    $ git push -u origin myfeaturebranch
    Enumerating objects: 8, done.
    Counting objects: 100% (8/8), done.
    Delta compression using up to 4 threads
    Compressing objects: 100% (4/4), done.
    Writing objects: 100% (6/6), 1.71 KiB | 878.00 KiB/s, done.
    Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
    remote: Resolving deltas: 100% (2/2), done.
    remote:
    remote: Create a pull request for 'myfeaturebranch' on GitHub by visiting:
    remote:      https://github.com/yelilo/Sf-Sandbox_Erika/pull/new/myfeaturebranch
    remote:
    To https://github.com/yelilo/Sf-Sandbox_Erika.git
    * [new branch]      myfeaturebranch -> myfeaturebranch
    Branch 'myfeaturebranch' set up to track remote branch 'myfeaturebranch' from 'origin'.
    ~~~
