# Práctica 1. Preparación de las herramientas.
En primer lugar, descargamos la ISO de **Ubuntu Server** y procedemos a realizar la instalación siguiendo los pasos habituales.
A continuación se muestran algunos pasos de la misma:
![Captura1](Imagenes/Captura1.png "Introducimos el nombre de la máquina")
![Captura2](Imagenes/Captura2.png "Seleccionamos el disco donde se realizará la instalación")
Una vez hemos llegado al paso en el que debemos seleccionar los programas *extra* a instalar, marcamos **OpenSSH** y **LAMP** (Apache, MySQL, PHP).
![Captura3](Imagenes/Captura3.png "Elegimos OpenSSH y LAMP para que se instalen")
![Captura4](Imagenes/Captura4.png "Establecemos una contraseña para la base de datos MySQL")
Al completar la instalación, lo primero que debemos hacer es definir una **contraseña** para el usuario **root** con `sudo passwd root`.
![Captura5](Imagenes/Captura5.png "Establecemos la contraseña para el root")
Mostramos la versión de **Apache** con el comando `apache2 -v`.
![Captura6](Imagenes/Captura6.png "Consultamos la versión de Apache")
Podemos ver que Apache se encuentra en ejecución con `ps aux | grep apache`.
![Captura7](Imagenes/Captura7.png "Mostramos que Apache se encuentra en ejecución")
Creamos un **archivo HTML** para comprobar el funcionamiento de Apache.
![Captura8](Imagenes/Captura8.png "Creamos el archivo hola.html en /var/www/html/")
Consultamos la **ip** de la máquina virtual con el comando `ifconfig`. En el apartado *Red* de la configuración de la máquina virtual es importante haber seleccionado el **adaptador puente** (Bridge). Esto nos permitirá acceder a la ip de la máquina virtual en nuestra máquina host.
![Captura9](Imagenes/Captura9.png "Consultamos la ip de la máquina virtual")
Para terminar, ejecutamos en el host la orden `curl http://192.168.1.47/hola.html`. Se nos mostrará el contenido del archivo HTML que hemos rellenado antes.
![Captura10](Imagenes/Captura10.png "Usamos el comando curl para mostrar el contenido del archivo HTML")
También podríamos acceder desde el *navegador* de la máquina anfitrión para ver la página web generada.

Repetimos los mismos pasos para la creación de la segunda máquina virtual.

