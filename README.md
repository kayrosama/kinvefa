# Pasos para la instalación del Sistema Factora

Proyecto para control de negocios implementando sistema de inventario, ventas y facturacion:

# Instaladores

| Nombre                   | Instalador                                                                                                                                                                                                                     |
|:-------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| `Compilador`             | Python3 |
| `Frameworks`             | [Django](https://www.djangoproject.com/ "Django") |
| `Bootstrap`             | [SB Admin 2](https://startbootstrap.com/theme/sb-admin-2 "SB Admin 2") |
| `IDE de programación`    | Visual Studio Code, Sublime Text, Geany, Vim, etc.  Jamas usar nano. |
| `Motor de base de datos` | MariaDB, PostgreSQL, Sqlite3 |

# Pasos de instalación

##### 1) Descomprimir el proyecto en una carpeta de tu sistema operativo

##### 2) Preparar un entorno virtual para el proyecto

Para linux:

```bash
apt-get install -f -y python3-pip python3-venv 
.
mkdir /path/proyecto
cd /path/proyecto
.
python3 -m venv venv
source venv/bin/activate
```

##### 3) Instalar librerias del proyecto

Para windows:

```bash
python3 -m pip install -r requirements.txt
```

##### 4) Instalar el complemento de [weasyprint](https://weasyprint.org/ "weasyprint")

Si estas usando Linux debes instalar las [librerias](https://doc.courtbouillon.org/weasyprint/stable/first_steps.html#linux "librerias") correspondientes a la distribución que tenga instalado en su computador.

##### 5) Crear la tablas de la base de datos a partir de las migraciones

```bash
python manage.py makemigrations
python manage.py migrate
```

##### 6) Insertar datos en las entidades de los modulos de seguridad y usuario del sistema

```bash
python manage.py shell --command='from core.init import *'
```

##### 7) Insertar datos iniciales de categorías, productos, clientes, compras y ventas (Paso opcional)

```bash
python manage.py shell --command='from core.utils import *'
```

##### 8) Iniciar el servidor del proyecto

```bash
python manage.py runserver 
```

Si deseas verlo en toda tu red puedes ejecutarlo asi:

Opcion Uno (1):
```bash
python manage.py runserver 0:8000
```
Opcion Dos (2):
```bash
python manage.py runserver 0.0.0.0:8000
```

##### 9) Iniciar sesión en el sistema (Puede cambiar la clave y usuario que se crea en el archivo core/init.py del paso 7)

```bash
username: admin
password: IchiBan
```

------------

#  Gracias por su atencion ✅

***KSM, 2024.***
