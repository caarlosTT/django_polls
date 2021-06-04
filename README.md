# Bienvenido a la librería de encuestas en python

Comandos para la inicialización del proyecto:

1. Descargar el repositorio:
$ git clone https://github.com/caarlosTT/django_polls.git

2. Crear el entorno virtual:
$ python3 -m venv .venv

3. Activar el entorno virtual:
$ source .venv/bin/activate

4. Instalar las librerias necesarias que se encuentran en el fichero 'requirements.txt':
$ pip install -r requirements.txt

5. Ejecutar las migraciones:
$ python3 manage.py migrate
Debará crearse un nuevo documento llamado 'db.sqlite3'

6. Cargar los datos iniciales:
$ python3 manage.py loaddata fixtures/polls_data.json

7. Configurar localhost como ip permitida para django:

Editar el fichero 'django_polls/settings.py'. Modificar la linea 28 añadiendo a la variable 'ALLOWED_HOSTS' la ip local.
ALLOWED_HOSTS = ['192.168.33.10', '127.0.0.1']

8. Iniciar el servidor:
$ python3 manage.py runserver