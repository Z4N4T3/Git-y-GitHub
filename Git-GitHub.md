# Sistema de control de versiones

## ¿Que es un sistema de control de versiones?

Un sistema de control de versiones nos ayuda a guardar el historial de cambios y crecimiento de los archivos de nuestro proyecto.

En realidad, los cambios y diferencias entre las versiones de nuestros proyectos pueden tener **similitudes**, algunas veces los cambios pueden ser solo una **palabra** o una parte específica de un archivo específico.

# Tipos de archivos y sus diferencias
 * **Archivos de texto (.txt)** : Texto plano normal y sin nada especial. Lo vemos igual sin importar de donde lo abramos, ya sea con el bloc de notas o con editores de texto avanzados.

 * **Archivos RTF (.rtf)** : Podemos guardar texto con diferentes tamaños, estilos y colores. Pero si lo abrimos desde un editor de código, vamos a ver que es mucho mas complejo que solo el texto plano. Esto es porque debe de guardar todos los estilos del texto y para esto, usa un código especial un poco difícil de entender y muy diferente a los textos con estilos especiales al que estamos acostumbrados.

 * **archivos en word (.docx)**: Podemos guardar imágenesy texto con diferentes tamaños, estilos o colores. Al abrirlo desde un editor de código podemos ver que es código binario, muy dificil de entender y muy diferente al texto que estamos acostumbrados. Esto es porque **Word** esta optimizado para entender este código especial y representarlo gráficamente. 



# Git
```
sudo apt update
sudo apt-get upgrade
sudo apt-get install git
git --version
```

![logo Git](https://git-scm.com/images/logo@2x.png)

Git es un software de control de versiones de código de forma distribuida.

Git está optimizado para guardar todos estos cambios de forma **atómica** e incremental,
es decir, aplicando cambios sobre los últimos cambios, esto sobre los cambios anteriores y así hasta el inicio de nuestro proyecto.

## Características
- Es muy **potente**.
- Fue diseñado por **Linus Torvalds**.
- No depende de un repositorio central.
- Es software libre.
- Se puede mantener un historial completo de versiones
- Es muy **rápido**.

Se obtiene una mayor eficiencia con archivos de texto plano, ya que con archivos binarios no se pueden guardar solo los cambios, sino que debe volver a grabar el archivo completo ante cada modificación, por mínima que sea, lo que hace que incremente demasiado el tamaño del **repositorio**.

Guardar archivos binarios en el repositorio de git es una mala práctica, únicamente deberían guardarse archivos pequeños que no sufran casi modificaciones durante la vida del proyecto. Los binarios deben de guardarse en un **CDN** (*Content Delivered Network* ).

# GitHub
![GitHub Logo](https://global-uploads.webflow.com/5f5a53e153805db840dae2db/6073fbf151fa4565d48572dc_GitHub_aprender-programaci%25C3%25B3n.jpeg)
**GitHub** es una plataforma de desarrollo colaborativo para alojar proyectos utilizando el sistema de control de versiones **git**. Se emplea principalmente para la creación de código fuente de programas de computadora.

A veces, **GitHub** se le considera como una red social de código para los programadores y en muchos casos es visto como un tu CV, pies aqui guardas tu portafolio de proyectos de programación.

# Algunos comandos básicos de la terminal Linux basadas en debian

* `pwd` : Nos muestra la ruta de carpetas en la que nos encontramos en el momento.

- `cd` : nos permite navergar entre los directorios/carpetas.

- `cd /` : nos dirige al directorio **raiz**.

- `cd /carpeta/subcarpeta` : Navega a una ruta dentro de la carpeta en la cual estamos actualmente.

- `cd ..` : regresa una carpeta hacia atrás. si queres dirigirte al directorio en el que te encontras basta con solo un punto (`cd .`).

- `mmkdir` : Nos permite crear carpetas (por ejemplo: `mkdir Carpeta-importante`).

- `touch` : crear archivos (`touch archivo.txt`)

- `rm` : Borra archivos o carpetas (`rm archivo.txt`)

- `cat`: ver el contendio de un archivo (`cat nombre-archivo.txt`)

- `ls` : nos permite ver los archivos de la carpeta donde estamos ahora mismo. Podemos usar uno o mas argumentos para ver más información sobre estos archivos (los argumentos pueden ser `--` + el nombre del argumento o `-` + una sola letra o shortcut por cada argumento).

- `ls -a` : Muestra todos los archivos, incluso los ocultos.

- `ls -l` : muestra los archivos de la carpeta enlistados. sin incluir los ocultos.

- `ls -la` : Muestra en lista todos los archivos, incluyendo los ocultos.

- `history` : Ver los últimos comandos que se ha ejecutado y un numero especial de asignacion que podemos repetir su ejecución con: `!(numero)` ejemplo (`!50`)

- `clear` : para limpiar pantalla o **Ctrl + L** .

# Conceptos importantes de Git
* **Staging** :recordar agregar definición

- **Bug**: Error en el código.
- **Repository**: Es donde se almacena todo el proyecto, el cual puede vivir tanto en local como en remoto. El repositorio guarda un historial de versiones y, más importante, de la relación de cada versión con la anterior para que pueda hacerse un árbol de versiones con las diferentes ramas.
- **Fork**: Si en algún momento queremos contribuir al proyecto de otra persona o si queremos utilizar el proyecto de otro como el punto de partida del nuestro. Esto se conoce como "Fork".

- **clone**: Una vez se decide hacer un **fork**, hasta ese momento sole existe en **GitHub**. Para poder trabajar en el proyecto, toca colar el repositorio elegido al computador personal.

- **branch**: Es una bifurcación del proyecto que se está realizando para anexar una nueva funcionalidad o corregir un **bug**.
- **master**: rama donde se almacena la ultima versión estable del proyecto que se está realizando. la rama **master** es la que se está en producción en cada momento(o casi) y devería de estar libre de **bugs**. Así. si esta rama está en producción, sirve como referente para hacer nuevas funcionalidades y/o arreglar bugs de última hora.
- **commit**: Consiste en subir cosas a la versión local del repositorio. De esta manera se puede trabajar en la rama local sin tener que modificar ninguna versión en remoto ni tener que tener la última version remota, cosa muy útil en grandes desarrollos trabajados por varias personas.

- **push** : Consiste en enciar todo lo que se ha confirmado con un **commit** al repositorio remoto. Aqui es donde se une nuestro trabajo con el de los demás.

- **checkout** : Acción de descargarse una rama del repositorio **GIT** local (si, git tiene su propio repositorio en local para poder ir haciendo **commits**) o remoto.
- **fetch** : Actualiza el repositorio local bajando datos del repositorio remoto al repositorio local sin actualizarlo, es decir, se guarda una copia del repositorio remoto en local.

- **merge**: La acción de **merge** es la continuación natural del **fetch**. El merge permite unir la copia del repositorio remoto con tu repositorio local, mezclando los diferentes códigos.

- **pull**: Consiste en la unión del **fetch** y del **merge**, esto es, recoge la informacion del repositorio remoto y luego mezcla el trabajo en local con esta.

- **diff** : Se utiliza para mostrar los cambios entre dos versiones del mismo archivo.

## Comandos básicos

* El comando para iniciar nuestro repositorio o indicarle a Git que queremos usar su **sistema de control de versiones** en nuestro proyecto es: 

>`git init`
* El comando para que nuestro repositorio sepa de la existencia de un archivo o sus ultimos cambios es:

> `git add`

Este comando no almacena las actualizaciones de forma definitiva, únicamente las guarda en algo que se conoce como *"Staging area"* (Area de montaje o ensayo).

* El comando para almacenar definitivamente todos los cambios que por ahora viven en el "*staging area*" es:

>`git commit`

Tambien podemmos guardar un mensaje para recordar muy bien que cambios hicimos en este commit con el argumento:

>`-m "mensaje del commit"`

>`git commit -m "mensaje del commit"`

* Por ultimo, si queremos mandar nuestros commits a un servidor remoto, un lugar donde todos podamos conectar nuestros proyctos, usamos el comando 
> `git push`


## Lista de comandos básicos de Git

`git init` :Inicializa un repositorio de **Git** en la carpeta donde se ejecute el comando.

`git add` : añade los archivos especificados al area de preparacion (*staging*)

`git commit -m "commit description"` : confirma los archivos que se encuentran en el area de preparacion y los agrega al repositorio. 

`git commit -am "commit description"` : añade al *staging area* y hace un commit mediante un solo comando (no funciona con archivos nuevos).

`git status` : ofrece una descripcion del estado de los archivos (*untracked, ready to commit, nothing to commit*).

`git rm <file/path name> (-cahed)` : remueve los archivos del **index**.

`git config --global user.email MyEmail@email.com` : configura un **email**.

`git config --global user.name <Nombre como se vera en los commits>` :  
configura un nombre

`git config --list` : Tira un listado de las configuraciones.

## Analizar cambios en los archivos de un proyecto Git

`git log` : lista de manera descendente los commits realizados.

`git log --stat` : además de listar los commits, muestra la cantidad de **bytes** añadidos y eliminados en cada uno de los archivos modificados.

`git log --all --graph --decorate --oneline` : Muestra de manera comprimida toda la historia del repositorio de manera gráfica y embellecida.

`git show <filename>` : Permite ver la historia de los cambios en un archivo.

`git diff <commit1><commit2>`: Compara las diferencias entre los commits, commit y arbol de trabajo, etc.

## Volver al tiempo con branches y checkout

`git reset <coomit>--soft/hard` : regresa al commit especificado, eliminado todos los cambios que se hicieron después de ese commit.

`git checkout <commit/branch><filename>`: Permite regresar al estado en el cual se realizó un commit o branch especificado, pero no elimina lo que está en el *staging area*.

`git checkout -<filePath>` :deshacer cambios en un archivo en estado *modified* (que ni fue agregado al *staging arean*).

## git rm y git reset
`git rm`

Este comando nos ayuda a eliminar archivos de **Git** **sin eliminar su historial del sistema de versiones**. Esto quiere decir que si necesitamos recuperar el archivo solo debemos "viajar en el tiempo" y recuperar el último commit antes de borrar el archivo en cuestión.

`git rm` no puede usarse por sí solo. Se debe utilizar uno de los flags para indicar a **git** como eliminar los archivos que ya no se necesitan en la ultima versión del proyecto.

* `git rm --catched <archivo/s>` : elimina los archivos del area de *staging* y del proximo commit, pero los mantiene en nuestro disco duro.

* `git rm --force <archivo/s>` :Elimina los archivos de **Git** y del disco duro. **Git** siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos , de modo que podremos recuperarlos si es necesario (Pero se decen aplicar comandos más avanzados) 

## git reset

Con `git reset` volvemos al pasado sin la posibilidad de volver al futuro. Borramos la historia y la debemos de sobreescribir.

* `git reset --soft` : Vuelve el branch al estado del **commit** especificado, manteniendo los archivos en el directorio de trabajo y lo que haya en *staging* considerando todo como nuevos cambios. Asi podemos aplicar las últimas actualizaciones a un nuevo **commit**.
* `git reset --hard` : Borra absolutamente todo. Toda la información de los commits y del area de *staging* se borra el historial.
* `git reset HEAD` : No borra los archivos ni sus modificaciones, solo los saca del area de *staging*, de forma que los ultimos cambios de estos archivos no se envíen al ultimo **commit**. Si se cambia de opinión se los puede incluir nuevamente con `git add` .

## Ramas o Branches de Git

Al crear una nueva rama se copia el último **commit** en esta nueva rama. Todos los cambios hechos en esta rama no se reflejarán en la rama master, hasta que hagamos un **merge**.
* `git branch <newbranch>` : Crea una nueva rama.
* `git checkout <branch_name>`: Se mueve a la rama específicada
* `git merge <branch_name>` : Fusiona la rama actual con la rama especificada y produce un nuevo **commit** de esta fusión 
* `git branch` : lista las ramas generadas

