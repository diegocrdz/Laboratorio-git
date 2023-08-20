<span style="font-family: Verdana;">

# Laboratorio-git

---

<span style="font-family: Times New Roman;">

**Bloque:**
Modelación de la Ingeniería y Ciencias

**Nombre del entregable:**
Laboratorio Git: Resumen

**Grupo:**
105

**Profesor:**
Octavio Navarro

**Alumno:**
Diego Córdova Rodríguez, A01781166

<span style="font-family: Verdana;">

---

# ¿Qué es GitHub? :monocle_face:

>**Github** es un sitio web mediante el cual se pueden crear repositorios; es decir, un lugar en el que puedes almacenar archivos y su respectivo historial de revisión.

A través de los repositorios se puede trabajar en equipo, colaborar, trabajar en distintas revisiones o versiones de un mismo archivo, etc. Finalmente, se puede subir, descargar o clonar el repositorio <span style="color:blue;">(mediante comandos en git o integraciones de Visual Studio Code).

![Logo de GitHub](images/githubLogo.png)
*Logo de GitHub*

---

# Bitácora de progreso :chart_with_upwards_trend:

A lo largo de estas clases, nos hemos adentrado a los aspectos más básicos de Github; es decir, lo que comprende crear un repositorio.

Inicialmente, empezamos creando el repositorio directamente en GitHub. En mi caso fue nombrado como Laboratorio-git.

## Día 1

### Instalar Homebrew :arrow_down:

**macOS:**
Entrar a la terminal a través del buscador de Spotlight. Una vez dentro, insertar el siguiente comando:
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`.

**Windows**
No es necesario, se hace directamente desde el instalador

### Instalar Git :arrow_down:

**macOS**
En la terminal, insertar el comando `$ brew install git` para instalar la última versión de git.

**Windows**
Entrar a la [página oficial de Git](https://git-scm.com/downloads) y descargar el instalador para Windows.
**Una vez en el instalador no se debe cambiar nada más que el siguiente apartado:**
![](images/instalador.png)

### Nombre y correo en Git :email:

Una vez Git está instalado, insertar los siguientes comandos:
`git config --global user.name “Nombre de usuario”`
`git config --global user.email “Email de usuario”`

*En el caso de MacOS, se seguirá trabajando en la terminal*
*En el caso de Windows, se hace en Git*

### Crear SSH :key:

Secure SHell *(protocolo de red destinado a la conección con una computadora para acceder a ella a través de comandos)*.

**1. Generar SSH**

`ssh-keygen -t ed25519 -C "your_email@example.com"`

Después nos preguntó si deseabamos poner una contraseña para ejecutar cualquier acción futura; sin embargo, decidí no poner una por el momento.

**2. Verificar creación de SSH**

`eval "$(ssh-agent -s)"`

**3. Copiar SSH al portapapeles**

`ssh-add ~/.ssh/id_ed25519`

**4. Pegar SSH en GitHub**
Configuration/SSH & GPG Keys/New SSH Key

---

## Día 2

### Crear y clonar repositorio :floppy_disk:

Una vez creado y agregado el acceso por SSH, creamos una carpeta local y accedemos a ella a través del comando
`cd (ubicación de la carpeta)`

Algunos otros comandos importantes para ubicarla y revisar los archivos son los siguientes:
- `pwd`: imprime la carpeta en la que estoy trabajando en este momento
- `ls` - list: muestra los contenidos de la carpeta en la que estoy en este momento
- `ls -a`: list all - ver todos los archivos de la carpeta
- `cd "carpeta"`: changedirectory - le digo a qué carpeta me quiero mover
- `cat`: ver el contenido de un archivo

### Clonar a un repositorio local

Estando dentro de la carpeta en la que se desea clonar el repositorio (Con el comando `cd "carpeta"`), usar el comando `git clone (url del repositorio)` para clonarlo a la carpeta local que creamos anteriormente.

*La url del repositorio se encuentra en la página main del repositorio en GitHub*.

---

## Día 3

### Subir contenido al repositorio :arrow_up:

Una vez clonado el repositorio de forma local, empezamos a subir archivos a la carpeta del repositorio, así como empezamos a editar algunos otros como es este propio archivo **README**.

Entre los comandos que utilizamos en esta última fase, se encuentran los siguientes (ejecutar en este orden):

- `git add -A`: Subir todos los cambios realizados a la zona de pruebas de git
- `git commit -m "Descripción"`: Comentar los cambios realizados. Se suben los cambios al repositorio local
- `git push -u origin main`: Sube todos los cambios ya comentados a la rama main del repositorio en Github.

---

# Referencias

- [Descargar Git](https://git-scm.com/downloads)
- [¿Qué son los repositorios?](https://docs.github.com/en/repositories/creating-and-managing-repositories/about-repositories)
- [Markdown Guide](https://www.markdownguide.org/)