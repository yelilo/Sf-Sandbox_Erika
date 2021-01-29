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
> git brach

Puedes visualizar las ramas existentes

Genera una nueva rama con las siguientes lineas
1. > git branch _Nombre_de_la_rama_
2. > git checkout _Nombre_de_la_rama_
