### Usamos de base el ultimo trabajo de tomcat.

# Despliegue de una aplicación Python con Flask y Gunicorn

## Instalacion de python
- Lo primero que tenemos que hacer es instalar el gestor de paquetes de Python. (pip)
![instalar el gestor de paquetes de Python](assets/img/instalarGestorPython.png)
- Tambien nos descargamos pipenv para gestionar entornos virtuales.
![instalar pipenv](assets/img/intalarpipenv.png)
- Comprobamos que esta instalado bien.
![Comprobacion Instalacion](assets/img/ComprobarInstalacion.png)
- Lo siguiente es intalarnos python-dotenv para variables de entorno.
![python-dotenv](assets/img/dontenv.png)

## Creacion
- Creamos el directorio de la applicacion. (sudo mkdir -p /var/www/'nombre'), al 
crearla con sudo los permisos son de root lo vamos a cambiar para que pueda ser leido por todos.
(sudo chmod -R 775 /var/www/'nombre')
![Creacion Carpeta y permisos](assets/img/creacion.png)
