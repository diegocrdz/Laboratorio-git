# Laboratorio-git
Diego Córdova Rodríguez, A01781166

## ¿Qué es Github? :exploding_head:

Github es un sitio web mediante el cual se pueden crear repositorios; es decir, un lugar en el que puedes almacenar archivos y su respectivo historial de revisión.

A través de los repositorios se puede trabajar en equipo, colaborar, trabajar en distintas revisiones o versiones de un mismo archivo, etc. Finalmenre, se puede subir, descargar o clonar el repositorio (mediante comandos en git o integraciones de Visual Studio Code).

## Bitácora de progreso

A lo largo de estas clases, nos hemos adentrado a los aspectos más básicos de Github; es decir, lo que comprende crear un repositorio.

Inicialmente, empezamos creando el repositorio directamente en GitHub. En mi caso fue nombrado como Laboratorio-git.

### Instalar Homebrew

Después de esto, entramos en la terminal; lugar en el que en mi caso, al tener macOS, tuve que instalar Homebre a través del comando `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`.

### Instalar git

Después de instalar Homwbrew, inserté el comando `$ brew install git` para instalar la última versión de git.

### Nombre y correo en git

Inserté dos comandos, uno para establecer mi nombre y otro para mi correo.
Los comandos son los siguientes:
`git config --global user.name “<Nombre del usuario>”`
`git config --global user.email “<Email del usuario>”`

### Acceso por SSH

Para acceder por Secure SHell (protocolo de red destinado a la conección con una computadora para acceder a ella a través de comandos), usamos el siguiente comando:
`ssh-keygen -t ed25519 -C "your_email@example.com"`
En este código, tuvimos que poner nuestro correo registrado en Github.
Después nos preguntó si deseabamos poner una contraseña para ejecutar cualquier acción futura; sin embargo, decidí no poner una por el momento.

Una vez hecho esto, se entró a la configuración de Github y copiamos la llave SSH pública.

### Clonar repositorio

Una vez creado y agregado el acceso por SSH, creamos una carpeta local y accedimos a ella a través del comando `cd (ubicación de la carpeta)``

Algunos otros comandos importantes para ubicarla y revisar los archivos son los siguientes:
- `pwd`: imprime la carpeta en la que estoy trabajando en este momento
- `ls` - list: muestra los contenidos de la carpeta en la que estoy en este momento
- `ls -a`: list all - ver todos los archivos de la carpeta
- `cd`: changedirectory - le digo a qué carpeta me quiero mover
- `cat`: ver el contenido de un archivo

Finalmente usamos el comando `git clone` seguido de la url del repositorio para clonarlo a la carpeta local que creamos anteriormente.

### Subir contenido al repositorio

Una vez clonado el repositorio de forma local, empezamos a subir archivos a la carpeta del repositorio, así como empezamos a editar algunos otros como es este propio archivo **README**.

Entre los comandos que utilizamos en esta última fase, se encuentran los siguientes (ejecutar en este orden):

`git add -A`: Subir todos los cambios realizados a la zona de pruebas de git
`git commit -m "Descripción"`: Comentar los cambios realizados. Se suben los cambios al repositorio local
`git push -u origin main`: Sube todos los cambios ya comentados a la rama main del repositorio en Github.

![Logo de GitHub](images/githubLogo.png)
*Logo de Github*

## Referencias

- [Markdown Guide](https://www.markdownguide.org/)
- [¿Qué son los repositorios?](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories)