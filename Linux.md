Nos permite visualizar el contenido de un archivo de texto sin la necesidad de un editor.
```
cat prueba.txt
```

ls (de listar), permite listar el contenido de un directorio o fichero
```
ls
```

pwd Pwd (de print working directory o imprimir directorio de trabajo), es un conveniente comando que imprime nuestra ruta o ubicación al momento de ejecutarlo, así evitamos perdernos si estamos trabajando con múltiples directorios y carpetas.
```
pwd
```


cd (de change directory o cambiar directorio), es como su nombre lo indica el comando que necesitarás para acceder a una ruta distinta de la que te encuentras. Por ejemplo, si estas en el directorio /home y deseas acceder a /home/ejercicios, seria:
```
cd ejercicios
```
Regresar a la directorio anterior
```
cd ..
```

Touch crea un archivo vacío
```
touch /home/prueba1.txt
```

Mkdir (de make directory o crear directorio), crea un directorio nuevo tomando en cuenta la ubicación actual
```
mkdir /home/NewFolder
```

Eliminar archivos Remove
```
rm /home/MyFile.txt
```

La opción -r borra todos los archivos y directorios de forma recursiva. Por otra parte, -f borra todo sin pedir confirmación. Estas opciones pueden combinarse causando un borrado recursivo y sin confirmación del directorio que se especifique. Para realizar esto en el directorio respaldos ubicado en el /home, usamos:
```
rm -fr /home/respaldos
```



Cp (de copy o copiar), copia un archivo o directorio origen a un archivo o directorio destino. 
```
cp /Origen/prueba.txt /Destino/respaldo/prueba.txt
```

Cp con la opción -r que copia no sólo el directorio especificado sino todos sus directorios internos de forma recursiva.
```
cp -r /home/ejercicios /home/respaldos/
```

Mv (de move o mover), mueve un archivo a una ruta específica, y a diferencia de cp, lo elimina del origen finalizada la operación. Por ejemplo:
```
mv /home/prueba.txt /home/respaldos/prueba2.txt
```
cp -fr /mnt/* /var/lib/tftpboot/
