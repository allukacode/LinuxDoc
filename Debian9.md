# Debian 9 
### Documentacion Basica De Comandos Esenciales

Que Hacer despues de instalar Debian ?
Reiniciar / Apagar
```
sudo reboot

sudo poweroff
```


Actualizar las listas de paquetes de software.
```
sudo apt-get update
```

Actualiza los paquetes de software 
```
sudo apt-get upgrade

```
#Aplicaciones Esenciales del S.O
```
apt-get install apt-transport-https
apt-get install git
apt-get install net-tools
```

Forzar Instalacionnn
```
apt-get install -f
```








Instalar Un paquete con extension .deb
```
dpkg -i /home/guest/Downloads/google-chrome-stable_current_amd64.deb
o navegar hasta la carpeta donde se encuentra el .deb
/home/guest/Downloads# dpkg -i google-chrome-stable_current_amd64.deb

```
sudo apt-get update && sudo apt-get install apt-transport-https
apt --fix-broken install


sudo 

------------

dpkg: Como usar la herramienta para manejo de paquetes .deb

P. Como puedo instalar y desinstalar paquetes DEB en Debian o sus derivados.

R. La forma natural de hacerlo es usando la herramienta dpkg como veremos en estos pocos ejemplos.

Instalar con dpkg

dpkg -i nombre-del-paquete-deb

Comprobar la instalación

dpkg -l | grep nombre-del-paquete-deb

Deberías ver ii delante del nombre del paquete en la salida en pantalla, ello significaría que el programa ha sido correctamente instalado.

Desinstalar con dpkg

dpkg -r nombre-del-paquete-deb

Este comando removerá el paquete, pero dejara los archivos de configuracion intactos, esto es util en caso que hubieras realizado cambios en ellos y quieras una copia para usos posteriores. Pero si deseas quitar todo rastro del paquete debes usar purge

dpkg -P nombre-del-paquete-deb

Ahora no quedará rastro del paquete antes instalado.

---
sudo apt-get install -f



