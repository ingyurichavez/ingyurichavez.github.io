# GIT
- Es un sitema de control de versiones

# Instalacion
- https://git-scm.com/

# software de ayuda
- Sourcetree
    - gratis
    - https://www.sourcetreeapp.com/

# Flujo de trabajo
- working directory
    - mi carpeta de trabajo
- Staging area
    - Area temporal
    - guarda los cambios que realizamos en nuestra carpeta de trabajo
- Repositorio
    - Local
    - Remoto
        - GitHub

# Buenas practicas
- siempre crear una rama master secundaria
- hacer pruebas en la master secundaria probarlo y recien pasarlo a la master

# Comandos principales
_Local_
    git init
        `inicia un repositorio`
        `crea la carpeta oculta .git`
        `solo se hace una vez, al principio de un proyecto`
    git status
        `busca si hay cambios`
    git add .
        `envia al area temporal`
        `el punto indica que agrega todo`
        `[nombreArchivo.txt], puedo agregar solo un archivo en especial`
    git rm --cached nombreArchivo
        `saca del staging area un archivo o carpeta`
    git commit -m "texto descriptivo"
        `envia al repositorio`
        `[-m], para poner mensaje descriptivo`
    git log
        `lista los commits realizados`
        `[--oneline], muestra cada commit en una linea`
    git reset --hard 8c87cfa
        `Regresar a un punto de los commit`
        `[8c87cfa],  es un identificador`
        `cada commit tiene un identificador`
_Ramas_
    git branch miPrimeraRama
        `crear una rama`
    git checkout miPrimeraRama
        `entrar a una rama`
    git branch
        `indica en que rama estamos`
        `y cuantas ramas tenemos`
    git merge miPrimeraRama
        `tenemos que estar en el master`
        `siempre hacer antes un pull`
    git branch -d miPrimeraRama
        `eliminar una rama`

_Remoto_
    git push
        `envia al repositorio remoto`
    git pull
        `trae los cambios del repositorio remoto`
    git fetch
        `revisa si hay cambios en el repositorio local y remoto`

_GitHub_
    ingyurichavez@gmail.com / Varsovia10G
    git remote add origin https://github.com/ingyurichavez/git.git
    git push -u origin master

_Crear Versiones de nuestro Proyecto_
    _local_
    git tag version1.0 -m "Mi primera version"
    _Remoto_
    git push --tags
        `con [git push] no funciona`

_.gitignore_
    - crear archivo .gitignore
    - y dentro ponemos los archivos a ignorar


# Comandos Secundarios
_Version de git_
    git version
_Ayuda_
    git help
_configurar nombre y email_
    git config --global user.name "Yuri"
        `[--global] para toda la pc`
    git config --global user.email "ingyurichavez@gmail.com"
    git config user.name
        `ver nombre`
    git config user.name
        `ver el email`
    git config --list

_clonar_
    git clone [copiar la url del repositorio]
        `descargarlo por http`
        `tambien lo puedes descargar por ssh`
    git diff
        `muestra la diferencia entre lo que esta en el repo y tu pc`