# 2.- Sistemas de control de versiones: Git

Un Sistema de Control de Versiones (VCS por sus siglas en inglés) es una base de datos que registra todas las modificaciones realizadas sobre un conjunto de archivos a lo largo del tiempo. Históricamente, han existido tres generaciones de estos sistemas:

* **Locales:** Guardaban parches (diferencias) en el disco duro local. Si el disco fallaba, se perdía todo.
* **Centralizados (CVCS):** Sistemas como Subversion (SVN) donde existía un único servidor central con todos los archivos. Los clientes descargaban solo la última versión del archivo (checkout). Si el servidor caía, nadie podía trabajar.
* **Distribuidos (DVCS):** Aquí entra **Git**. En los sistemas distribuidos, los clientes no solo descargan la última versión, sino que replican (clonan) completamente el repositorio entero. Si el servidor central falla, cualquier repositorio local de cualquier trabajador puede copiarse de vuelta al servidor para restaurarlo.

**Origen y filosofía de Git:**
Git fue creado en 2005 por Linus Torvalds, el creador del kernel de Linux. El equipo de desarrollo de Linux necesitaba una herramienta rápida, descentralizada y capaz de manejar proyectos masivos, ya que las herramientas gratuitas de la época no daban la talla. A diferencia de otros sistemas que guardan la información como una lista de cambios en los archivos, Git modela sus datos como un conjunto de instantáneas (snapshots) de un mini sistema de archivos. Cada vez que guardas el estado de tu proyecto, Git toma una foto del aspecto de todos tus archivos en ese momento y guarda una referencia a esa instantánea.

Git opera principalmente en local, lo que significa que la mayoría de las operaciones son casi instantáneas porque no necesitan conexión a la red. Además, Git gestiona los archivos en tres estados principales:
1. **Modified (Modificado):** Has cambiado el archivo pero aún no lo has guardado en la base de datos de Git.
2. **Staged (Preparado):** Has marcado un archivo modificado en su versión actual para que vaya en tu próxima captura (commit).
3. **Committed (Confirmado):** Los datos están almacenados de forma segura en tu base de datos local.

<img src="img/git.png" alt="Logo de Git" width="400" height="250"/>
