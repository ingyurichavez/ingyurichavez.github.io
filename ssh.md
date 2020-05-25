# SSH
    - Secure Shell (Acceso seguro por consola)
    - Es un protocolo
    - sirve para conectarte a tu servidor por medio de terminal
    - sirve para administrar servidores
    - es mas rapido que ftp
    - sincronizar archivos, solo sube lo necesario y no todo
    - descarga rapida de archivos de internet
    - conectar con mi repositorio
- ssh nace por la inseguridad de telnet
    - telnet es un protocolo para controlar una pc
    - enviar info por telnet
        - es como pasar info por una hoja, todos lo ven
    - enviar info con ssh
        - es enviar la hoja en un maletin con 2 candados
- Autenticacion por:
    - clave publica
        - para compartir con otras personas
    - privada
        - se queda con nosotros

# Software
- instalar servicio ssh
    - linux, ya viene instalado
    - windows, instalar putty
- usar vim
    - para editar codigo

# comandos
_Comandos Basicos_
    cd
        `entrar a una carpeta`
        `[..] lleva a un nivel mas arriba`
    ls
        `listar archivos y carpetas`
    mkdir NombreCarpeta
        `crea directorio`
    touch archivo.txt
        `crea archivo`
    mv archivo.txt prueba/archivo.txt
        `mueve archivo a una nueva ubicacion`
    cp archivo.txt prueba/archivo.txt
        `copia archivo a una nueva ubicacion`
    rm archivo.txt
        `borra un archivo`
    pwd
        `muestra en que carpeta estoy`

_pasar Certificado publico de mi pc al servidor_
    ssh-keygen
        `crea un certificado local de nuestra pc`
    cat .ssh/id_rsa.pub
        `copiar el sertificado publico en el servidor`
        `ojo: tu certificado privado nunca se copea en ningun lado`
        `copiar el contenido`
        vim .ssh/authorized_keys
            `aqui dentro pegamos el contenido`
    ahora entramos al servidor y no debe pedirnos contraseña