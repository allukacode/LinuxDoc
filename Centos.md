-Establecer Hora y Fecha al sistema F:"Año-Mes-Dia" - "Hora"
date --set "2018-06-10 11:20"


-Cambiar contraseña de usuario en centos
passwd allukacodee

-Instalar Archivos.Rpm
yum install http:urldelarchivo.rpm

- Actualizar Paquetes
yum update

-Para actualizar un paquete o paquetes específicos, pruebe lo siguiente:
yum update nameofpackage

- Cómo buscar actualizaciones usando YUM sin instalarlas
yum check-updates

- Cómo quitar programas que usan YUM
yum remove programname

-Para eliminar programas que dependen del programa que está eliminando con el siguiente comando:
yum autoremove programname

-Listar todos los paquetes RPM disponibles usando YUM puede enumerar todos los paquetes disponibles dentro de YUM simplemente usando el siguiente comando:
yum list
https://www.lifewire.com/install-rpm-packages-using-yum-2201155

-Firewall -> Abrir Puerto
sudo firewall-cmd --zone=public --add-port=1433/tcp --permanent
sudo firewall-cmd --reload

yum group list
-Saber modo de arranque
systemctl get-default
* multi-user.target (the command line), or
* graphical.target (the Windows-like GUI)
Cambiar modo
systemctl set-default multi-user.target
systemctl set-default graphical.target


Preveemos un posible error de repositorio
yum --enablerepo=base clean metadata

-Instalamos, hora de ir por un café ;-)
yum groupinstall 'Servidor con GUI'

