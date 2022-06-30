# TUTORIAL BÁSICO GIT


## CONFIGURACIÓN INICIAL DE GIT

* `git config --global user.name "Jose Antonio Sabino"`
* `git config --global user.email jantoniosabino@gmail.com`
* `git config --global core.editor "code --wait"` Esto es para indicar que usamos vscode
* `git config -e` Abre el archivo de configuración en el editor
* `git config --global core.autocrlf true` Para configurar los saltos de linea en auto, ya que dependiendo del S.O. de cada desarrollador guardará los caracteres especiales de salto de una forma diferente. Si estamos en windows usaremos "true", si estamos en mac usaremos "input"
* `git config -h` Muestra un listado de todas las configuraciones que podemos hacer

## GITBASH SISTEMA DE ARCHIVOS

| Sintaxis    | Descripción |
| ------    | ------            |
| `Ctrl + l` | Limpiar terminal |
| `pwd` | Muestra la ruta actual |
| `ls` | dir de ms-dos |
| `ls -a` | dir de ms-dos con archivos ocultos |
| `cd <folder>` | Ir a la carpeta |
| `cd .. <folder>` | Volver a la carpeta anterior |
| `mkdir <file>` | Crear directorio |
| `rm <file>` | Eliminar archivo |
| `mv <file>` | Mover archivo |
| `mv <file1> <file2>` | Renombrar archivo |
| `cat <file>` | Mostrar contenido de archivo |

## COMANDOS GIT

### CREAR REPOSITORIO

| Sintaxis    | Descripción |
| ------    | ------            |
| `git init`| Inicializar repositorio en el directorio actual |
| `git init <folder>`| Crear carpeta y inicializar repositorio en él |
| `git clone`| Hace copia del código del servidor a la computadora |

### OBSERVAR REPOSITORIO

| Sintaxis    | Descripción |
| ------    | ------            |
| `git status`| Ver el estado de los archivos, cuales están en staging o han cambiado |
| `git status -s`| status simplificado |
| `git diff` | Ver los cambios realizados en los archivos que no han pasado al stage (para salir del proceso pulsar "q") |
| `git diff --staged` |Ver los cambios realizados en los archivos que se encuentran en el stage (para salir del proceso pulsar "q") |
| `git diff <commit1> <commit2>` | Ver cambios entre dos commits |
| `git show`| - |
| `git log` | Ver historial de cambios |
| `git log -p <file / folder>` | Ver historail de cambios de un archivo o carpeta |
| `git log --oneline` | Muestra el historial simplificado  |

### HACER CAMBIOS

| Sintaxis    | Descripción |
|-------- | ---------- |
| `git add <file>`| Añadir al staging un archivo |
| `git add .`| Añadir al staging todos los archivos cambiados |
| `git commit -m "titulo descriptivo"` | Pasar del stagin al repositorio local (`-m` para dar título al snapshot) |
| `git reset <file>`| Eliminar archivo del staging |
| `git reset <commit>`| Volver a un commit anterior especificado |
| `git reset --hard`| Volver al ultimo commit guardado |

### SINCRONIZACION

| Sintaxis    | Descripción |
|-------- | ---------- |
| `git push`| Pasar al repositorio remoto |
| `git push -u origin master` | Subir cambios a servidor. Con `-u` creamos por primera vez la rama |
| `git push -u origin <rama>`| Subir otra rama |
| `git pull`| Trae los cambios de otros desarrolladores y los une a la rama|
| `git fetch`| Trae los cambios de otros desarrolladores y NO los une a la rama|

### RAMAS

| Sintaxis    | Descripción |
| ------    | ------            | 
| `git branch` | Ver en qué rama nos encontramos |
| `git branch` | Ver todas las ramas locales y remotas |
| `git branch <nuevaRama>` | Crear rama |
| `git branch -d <rama>` | Eliminar rama |
| `git checkout <rama>` | Cambiar de rama |
| `git checkout -b <rama>` | Crear una rama |
| `git merge <ramab>` | Traer los cambios de ramab a master (fusionar) |
| `git remote add origin https://github.com/jantoniosabino/gitApuntes.git` | Subir proyecto a servidor por primera vez |

## EL ARCHIVO .gitignore

En este archivo incluiremos todos los archivos y rutas que no queremos subir al repositorio
> Aquí puede añadir archivos de variables de configuración local, contraseñas, la carpeta /node_modules, etc... 
