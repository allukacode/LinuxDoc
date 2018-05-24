# Debian 9
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

Instalar Un paquete con extension .deb
```
dpkg -i /home/guest/Downloads/google-chrome-stable_current_amd64.deb
o navegar hasta la carpeta donde se encuentra el .deb
/home/guest/Downloads# dpkg -i google-chrome-stable_current_amd64.deb

```
sudo apt-get update && sudo apt-get install apt-transport-https
apt --fix-broken install

