https://docs.djangoproject.com/es/3.1/intro/tutorial01/

===============================
ACCESSO VIA Visual Studio
===============================

# Abrir en "Visual Studio" el folder de trabajo con un archivo .py cualquiera, puede ser vacio
# Se seleciona el interprete Python "Crtl+Shift+P" (apareceran todos los instalados, elegir el que tenga la versión que queremos)

py -3 --version    --> Windows
python3 --version  --> Linus

# Se abre un Termina de VSCode (Ctrl + Shift + ñ)
	cd "C:\Users\chimo\OneDrive\Escritorio\BIG_DATA\Python\WebDjango010"
# Se crea entorno virtual
	python -m venv envDj010
# Se activa el entorno virtual (puede ser que Visual Studio nos pregunte si usarlo después de crearlo, en cuyo caso no haría falta activarlo a mano).
	C:\Users\chimo\OneDrive\Escritorio\BIG_DATA\Python\WebDjango010\envDj010\Scripts\Activate.ps1

Debe cambiar el prompt a algo así:

(envDj010) PS  C:\Users\chimo\.....

De no ser asi, hay que hacer esto y despues abrir otro terminal:
	> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser 

pip search django 				--> Verificar que django está ya instalado en ese entorno virtual.

python -m pip install django			--> Si da error es porque hay que instalarlo:

django-admin startproject mysite		--> Para empezar un projecto de DJANGO

cd mysite

python manage.py runserver			--> Para verificar que DJANGO esta arrancado y funcionando --> la primera vez crea "db.sqlite3". Si funciona se tiene que abrir correctamente la pagina: http://127.0.0.1:8000/


Si nos da el problema "You have X unapplied migration(s)" es porque aun no se ha creado la base de datos, usamos:

python manage.py showmigrations --list    	--> Para ver que pasa
python manage.py migrate --plan			--> Para ver que pasa

python manage.py makemigrations    
python manage.py migrate			--> Para solucionarlo

Y volvemos a ejecutarlo para ver si se soluciono:

python manage.py runserver  			--> Si funciona se tiene que abrir correctamente la pagina: http://127.0.0.1:8000/

python manage.py runserver 5000			--> Por si se quiere cambiar el puerto.


python manage.py startapp polls			--> Crea aplicacion "polls" dentro del proyecto

python manage.py shell 				--> Permite a través de comando acceder a la base de datos (es una api de acceso).

pip install pylint-django			--> Me daba un error de que la clase Question no tenía objetos.

http://127.0.0.1:8000/admin/polls/question/
http://127.0.0.1:8000/polls/
http://127.0.0.1:8000/polls/1/results/
http://127.0.0.1:8000/polls/detail/

pip freeze > requirements.txt

>>>> ME QUEDE AQUI:
https://docs.djangoproject.com/es/3.1/intro/tutorial04/

NOTA: (No recuendo como era esto-->Interesante crear un JSON Python + DJANGO para "Run & Debug" --> Se hace en el icono debug de VScode

------------------------------------------------------------------------------------------

PARA SALIR DEL ENTORNO VIRTUAL SI FUESE NECESARIO:

>C:\Users\chimo\OneDrive\Escritorio\BIG_DATA\Python\WebDjango010\env010\Scripts\deactivate

o si no sale:

> exit
