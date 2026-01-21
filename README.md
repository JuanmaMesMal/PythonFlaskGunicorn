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
- Lo siguiente que hay que hacer es crear dentro de /var/www/'nombre' un archivo .env y modificarlo y poner dentro lo sigueinte que son las variables de entrorno,
![Archivo creado modificado env](assets/img/archivoenv.png)
- Despues de esto iniciamos nuestro entorno virtual 
    - Me estaba dando un error de permisos, y es que no he realizado un chown 
    ![error](assets/img/error.png)
![Arreglo](assets/img/arregloyentornovirtual.png)

- Dentro de la aplicacion necesitamos intalar las dependencias necesarias para este proyecto.
![Instalacion de flack y gunicorn](assets/img/intalacionflackgunicorn.png)
- a continuacino creamos dos archivos uno que es application.py y otro que es wsgi.py
![Creacio de archivos application y wsgi](assets/img/Creacionarvhicospy.png)
y editamos primero el de application.py y añadimos lo siguiente 
![Aplication.py](assets/img/applicationpy.png)
y despues el wsgy.py 
![wsgy.py](assets/img/wsgipy.png)

- Lo siguiente es iniciar la applicacion con flask
![Iniciar App](assets/img/IniciarApp.png)
luego con nuestra ip buscamos 'ip':5000
![App desplegada](assets/img/appdesplegada.png)
- y a continuacion lo hacemos con  gunicorn
![Iniciar app](assets/img/iniciamosgunicorn.png)
![App desplegada gunicor](assets/img/desplegadogunicorn.png)
