### Linux

------



### Indice

------

1. Termina o Consola
2. Estructura del terminal
3. 

### Terminal ó Consola

------

Los sistemas operativos basados en Unix disponen de un **intérprete de comandos u órdenes** (conocido como terminal, consola ó shell) que hace de interfaz entre el usuario y el propio sistema operativo. Es decir, mediante la terminal o consola podemos acceder al sistema operativo sin utilizar la interfaz gráfica y realizar todo tipo de tareas en modo texto. 



Podemos conectarnos a un host por medio del protocolo **SSH**

```
C:\GitHub\LinuxDoc> ssh guest@192.168.0.2
guest@192.168.0.2's password:
Last login: Mon Jun 25 15:51:34 2018 from 192.168.0.10
[guest@centos /]$
```



### Estructura del terminal

------

```
[NombreDeUsuario@Host:Directorio]$
```

**$** Usuario Estandar

**#** Usuario Administrador

```
[Usuario01@centos home]$
[Administrador@centos home]#
```



### Listar directorios y archivos 

------

Comando "ls" Lista el contenido de los directorios

Su sintaxis es: 

```
ls -opcion argumento
```



- **ls** Lista el contenido de los directorios (por defecto ordena la salida alfabéticamente). 

  ```
  [usuario01@centos ~]$ ls
  comandos.txt  Descargas  Documentacion.doc  Documentos  Escritorio  Imagenes  Musica  Videos
  ```

  **Opciones:**
  - **ls -a** Lista el actual directorio con archivos, incluyendo los archivos y directorios ocultos.
  - **ls -t** Ordena los archivos por fecha de modificación.
  - **ls -x** Ordena los archivos por extensión.
  - **ls -l** Muestra toda la información: usuario, grupo, permisos, tamaño, fecha y hora de creación.
  - **ls -lh** Muestra la misma información que ls -l pero con las unidades de tamaño en KB, MB, etc.
  - **ls -r** Muestra el contenido de todos los subdirectorios de forma recursiva.
  - **ls -s** Ordena los resultados por tamaño de archivo.
  - **-a** todos los archivos, incluso los que comienzan con punto (.).
  - **-A** Lista todos los ficheros en los directorios, excepto los que comienzan con punto . (.) y los que comienzan con doble punto (..).
  - **-F** indica tipo: / directorio, * ejecutable, @ enlace simbólico.
  - **-h** indicará el tamaño en KB, MB, etc.
  - **-l** listado en formato largo (o detallado).
  - -**S** clasifica los contenidos de los directorios por tamaños, con los ficheros más grandes en primer lugar.
  - **-r** invierte el orden de la salida.
  - **-R** Lista recursivamente los subdirectorios encontrados.
  - **-t** ordenar por fecha de última modificación.
  - **-u** ordenar por fecha de último acceso.
  - **-x** presenta los ficheros por columnas.
  - **-i** precede la salida con el número de **i-node** (ver el comando ln).

Listar un directorio Especifico

```
[usuario01@centos ~]$ ls /home/
usuario01  usuario02  usuario03  usuario04  usuario05  usuario06 
```

```
[usuario01@centos ~]$ ls -a
.   .bash_logout   .bashrc  comandos.txt  Descargas          Documentos  Imagenes  Musica
..  .bash_profile  .cache   .config       Documentacion.doc  Escritorio  .mozilla  Video
```

Cuando se lista un directorio 

```
[usuario01@centos ~]$ ls -l
total 0
-rw-rw-r--. 1 usuario01 usuario01 0 Jun 25 16:31 comandos.txt
drwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:24 Descargas
-rw-rw-r--. 1 usuario01 usuario01 0 Jun 25 16:31 Documentacion.doc
drwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:25 Documentos
drwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:25 Escritorio
drwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:25 Imagenes
drwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:25 Musica
drwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:25 Videos
```

El **primer** carácter de cada línea indica el **tipo de fichero** 

**- **   rw-rw-r--. 1 usuario01 usuario01 0 Jun 25 16:31 comandos.txt
**d**   rwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:24 Descargas
**-**    rw-rw-r--. 1 usuario01 usuario01 0 Jun 25 16:31 Documentacion.doc
**d**   rwxrwxr-x. 2 usuario01 usuario01 6 Jun 25 16:25 Documentos

-  **-**  Fichero regular. 
- **d**  Directorio
- **l**  Enlace simbólico (ver el comando ln). 
- **c**  Dispositivos de caracteres 
- **b**  Dispositivos de bloques. 
- **s** Conexiones con el dominio local. 
- **p** Conexiones. 

### Navegar entre los directorios

------



- **cd**   (Change Directory) Cambiar de directorio 

  ```
  [usuario01@centos Descargas]$ cd /home/usuario01/Escritorio
  [usuario01@centos Escritorio]$
  ```

- **cd ..** (Back) Regresar al directorio anterior

  ```
  [usuario01@centos ~]$ cd ..
  [usuario01@centos home]$
  ```

### Informacion del sistema

------



- pwd **  (Print Working Directory)  Ubicacion del directorio actual

```
[usuario01@centos Descargas]$ pwd
/home/usuario01/Descargas
```

- **whoami**  (Who am i?) Usuario que estamos usando

```
[usuario01@centos Descargas]$ whoami
usuario01
```

- **hostname**  Nombre del host

```
[usuario01@centos Descargas]$ hostname
centos
```

- **cat**   Permite visualizar el contenido de un archivo

```
[root@centos ~]# cat .bash_history
apt-get install git
yum install git
yum install openssh-server openssh-client
yum get-update
apt update
```

- **.bash_history** En este archivo se almacena todo el historial de comandos usados cuando se cierra session ( se puede modificar el tamaño max)

```
[root@centos ~]# cat .bash_history
```

- **history** Lista el historial de comandos
  - History -c ( Clear ) Limpiar el hostorial
  - history -w ( Write ) Guardar cambios en el archivo **.bash_history**

```
[root@centos ~]# history
    1  apt-get install git
    2  yum install git
    3  yum install openssh-server openssh-client
    ...
   839  yum install openssh-server openssh-client
   840  yum install openssh-server
```

```
[root@centos ~]# history -c
[root@centos ~]# history
    1  history
[root@centos ~]# history -w
[root@centos ~]# cat .bash_history
history
historty -w
```

