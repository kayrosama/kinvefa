# kinvefa
Sistema de Control
...
Este proyecto inicia con la necesidad de controlar las operaciones diarias en las empresas.


# Pasos para instalar el Sistema

# Instaladores
| Nombre                   | Instalador                                                                                                                                                                                                                     |
|:-------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| `Compilador`             | Python3                                               |
| `IDE de programación`    | Visual Studio Code , Sublime Text , Atom , Vim , etc. |
| `FrameWorks` |  [Reflex](https://reflex.io/ "Reflex")                            |
| `Motor de base de datos` | MySQL , PostgreSQL , Sqlite3                          |

# Pasos de instalación
##### 1) Descomprimir el proyecto en una carpeta de tu sistema operativo
##### 2) Crear un entorno virtual para posteriormente instalar las librerias del proyecto
Linux:
```bash
apt-get install -f -y python3-pip python3-venv
python3 -m venv venv
```

##### 3) Instalar el complemento de [weasyprint](https://weasyprint.org/ "weasyprint")
Linux debes instalar las [librerias](https://doc.courtbouillon.org/weasyprint/stable/first_steps.html#linux "librerias") correspondientes a la distribución que tenga instalado en su computador.

##### 4) Activar el entorno virtual de nuestro proyecto
Linux:
```bash
source venv/bin/activate
```

##### 5) Instalar todas las librerias del proyecto que se encuentran en la carpeta deploy

```bash
python3 -m pip install -r requirements.txt
```

##### 6) Crear la tablas de la base de datos a partir de las migraciones
```bash
python manage.py makemigrations
python manage.py migrate
```

##### 7) Insertar datos en las entidades de los modulos de seguridad y usuario del sistema
```bash
python manage.py shell --command='from core.init import *'
```

##### 8) Insertar datos iniciales de categorías, productos, clientes, compras y ventas (Paso opcional)
```bash
python manage.py shell --command='from core.utils import *'
```

##### 9) Iniciar el servidor del proyecto
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

##### 10) Iniciar sesión en el sistema (Puede cambiar la clave y usuario que se crea en el archivo core/init.py del paso 7)
```bash
username: admin
password: IchiBan
```

------------

#  Gracias por su atencion ✅🙏

***KSM, 2024.***


