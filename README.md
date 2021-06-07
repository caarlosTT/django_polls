# Bienvenido a la librería de encuestas en python

Comandos para la inicialización del proyecto:

1. Descargar el repositorio:
$ git clone https://github.com/caarlosTT/django_polls.git

2. Crear el entorno virtual:
$ python3 -m venv .venv

3. Activar el entorno virtual:
$ source .venv/bin/activate

4. Instalar las librerias necesarias que se encuentran en el fichero 
'requirements.txt':
$ pip install -r requirements.txt

5. Ejecutar las migraciones:
$ python3 manage.py migrate
Debará crearse un nuevo documento llamado 'db.sqlite3'

6. Cargar los datos iniciales:
$ python3 manage.py loaddata fixtures/polls_data.json

7. Configurar localhost como ip permitida para django:

Editar el fichero 'django_polls/settings.py'. Modificar la linea 28 
añadiendo a la variable 'ALLOWED_HOSTS' la ip local.
ALLOWED_HOSTS = ['192.168.33.10', '127.0.0.1']

8. Iniciar el servidor:
$ python3 manage.py runserver

## Instaacion de la aplicación en un servidor remoto con fabric:

1. Instalar fabric en el entorno virtual:
$ pip install fabric

2. Comprobar la dirección del repositorio de la aplicación en la línea 8
del fichero fabfile.py

3. Comprobar los datos del servidor remoto en las líneas 14, 15 y 16.

4. Iniciar la máquina que simulará el servidor remoto en otra consola:
$ ssh vagrant@192.168.33.10

4. Desplegar la aplicación mediante un comando en consola:
$ fab development deploy
