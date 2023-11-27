# Tienda Online - Proyecto-Unidad-IV

Este proyecto es una tienda online que incluye un sistema de inicio de sesión. A continuación, se proporciona una breve explicación del código relacionado con la página de inicio de sesión.

## Estructura del Código
### Archivo base.html
Este archivo sirve como plantilla base para otras páginas. Contiene bloques que se extienden y personalizan en otras plantillas. En este contexto, se utiliza para proporcionar la estructura básica de las páginas.


### Archivo login.css
Este archivo contiene estilos específicos para la página de inicio de sesión. Define la apariencia de los elementos como el contenedor de inicio de sesión, el título, el formulario y otros elementos visuales.


### Página de Inicio de Sesión (login.html)
Esta página presenta un formulario de inicio de sesión simple con campos para el nombre de usuario y la contraseña. Al enviar el formulario, los datos se envían al servidor utilizando el método POST y la acción "/login". El formulario incluye un botón "Login" que realiza la acción de enviar.

La página también maneja mensajes flash que podrían generarse durante el proceso de inicio de sesión, como mensajes de error.


## Detalles del Formulario
- **Username:** Campo de entrada de texto para el nombre de usuario.
- **Password:** Campo de entrada de contraseña para la contraseña del usuario.
- **Login Button:** Botón para enviar el formulario de inicio de sesión.


## Uso del Sistema de Mensajes Flash
El sistema de mensajes flash se utiliza para proporcionar retroalimentación al usuario. Los mensajes flash se generan en el servidor y se muestran en la interfaz de usuario. En este caso, se utiliza para mostrar mensajes de error durante el proceso de inicio de sesión.



# Catálogo de Productos - Administración
Catálogo de productos con funcionalidades de administración. A continuación, se proporciona una descripción del código relacionado con la administración de productos.

## Estructura del Código

### Archivo base.html
Este archivo sirve como plantilla base para otras páginas. Contiene bloques que se extienden y personalizan en otras plantillas. En este contexto, se utiliza para proporcionar la estructura básica de las páginas.


### Archivo style.css
Este archivo contiene estilos específicos para la página de administración de productos. Define la apariencia de los elementos como el formulario de agregado de productos, la lista de productos existentes y otros elementos visuales.


### Página de Administración (admin.html)
Esta página permite a los usuarios con roles de administrador agregar, editar y eliminar productos. Incluye un formulario para agregar nuevos productos y una lista de productos existentes con opciones de edición y eliminación.


## Detalles de la Página de Administración
- **Formulario para Agregar Productos:** Permite al administrador agregar nuevos productos proporcionando el nombre del producto, el precio y la URL de la imagen.

- **Lista de Productos Existentes:** Muestra una lista de productos existentes con detalles como el nombre, el precio y una imagen. Cada producto en la lista tiene opciones de eliminar y editar.

- **Edición de Productos:** Para cada producto en la lista, se proporciona un formulario de edición que aparece al hacer clic en el botón "Editar". Permite al administrador modificar el nombre, el precio y la URL de la imagen del producto.


## Funciones JavaScript Principales
- **checkUserLogin():** Verifica si el usuario ha iniciado sesión y tiene permisos de administrador. Si no, redirige al usuario a la página de inicio de sesión.

- **logout():** Elimina la información de inicio de sesión almacenada localmente y redirige al usuario a la página de inicio de sesión.

- **validateAndAddProduct():** Valida los campos del formulario de agregar producto y, si son válidos, agrega el producto a la lista.

- **updateProductList():** Actualiza la lista de productos en la página.

- **editProduct(productId):** Muestra el formulario de edición para un producto específico.

- **saveEditedProduct(productId):** Guarda los cambios realizados en el formulario de edición para un producto específico.

- **removeProduct(productId):** Elimina un producto de la lista.

- **clearForm():** Limpia el formulario de agregar producto.

- **saveProducts():** Guarda la lista de productos en el almacenamiento local.

- **updateProductList():** Actualiza la lista de productos en la página al cargar.

## Uso del Almacenamiento Local

La información sobre productos y roles de usuario se almacena localmente utilizando el almacenamiento local del navegador. Esto facilita la persistencia de datos entre sesiones.


# Tienda en Línea - Administrador

Este es el README para la versión del código de la tienda en línea destinada a administradores. Esta versión incluye funcionalidades específicas para la administración del catálogo de productos.

## Configuración del Entorno

Asegúrese de tener las siguientes dependencias instaladas:

- [Python](https://www.python.org/downloads/)
- [Flask](https://flask.palletsprojects.com/en/2.1.x/installation/)
- [Bootstrap 4](https://getbootstrap.com/docs/4.5/getting-started/introduction/)

## Estructura del Código

La aplicación utiliza Flask como framework de backend y Bootstrap 4 para el diseño del frontend. La estructura del código está organizada en bloques de Jinja y JavaScript, proporcionando una interfaz dinámica y atractiva.

## Funcionalidades Específicas del Administrador

### Verificación de Inicio de Sesión

La función `checkUserLogin()` asegura que solo los usuarios con roles de administrador (`"1"`) pueden acceder a las funciones administrativas. Si un usuario no ha iniciado sesión o no es un administrador, se redirige automáticamente a la página de inicio de sesión.

### Barra de Navegación

La barra de navegación incluye enlaces a secciones clave de la aplicación, como el catálogo de productos, la tienda y la calculadora. También se proporciona un botón para cerrar sesión.

### Catálogo de Productos

El enlace "Catálogo de Productos" lleva a los administradores a una página donde pueden gestionar y visualizar el catálogo de productos disponibles. Esta función está controlada por la ruta `admin` en la aplicación Flask.

### Calculadora Modal

Los administradores tienen acceso a una calculadora funcional mediante el botón "Calculadora" en la barra de navegación. Esta calculadora se presenta en un modal y permite realizar operaciones matemáticas simples.

### Cierre de Sesión

El botón "Cerrar Sesión" permite a los administradores cerrar sesión, redirigiéndolos a la página de inicio de sesión.

## Configuración de Estilos y Scripts

Los estilos y scripts necesarios para el funcionamiento adecuado de la aplicación se importan en el bloque `miCSS`. Se incluyen Bootstrap y otras dependencias para mejorar el diseño y la experiencia del usuario.

1. **Funcionalidades Específicas:**
   - Inicie sesión con credenciales de administrador.
   - Explore el catálogo de productos, la tienda y utilice la calculadora según sea necesario.


## Cómo Ejecutar el Proyecto
1. Entorno virtual, abrimos CMD como administrador y nos dirigimos a la carpeta donde se encuentra el proyecto y creamos el entorno virtual:
Crear un entorno virtual:
py -m venv env

Activar el entorno virtual:
env\Scripts\activate

Instalar Flask en el entorno virtual:
pip install Flask

Asignar el archivo principal
set FLASK_APP=app.py

2. Instala las dependencias del proyecto ejecutando `pip install Flask`,`pip install Flask_MySQL`,`pip install Flask-Login`.
3. Ejecuta la aplicación con el comando `flask run.`.
4. Abre tu navegador y visita `http://127.0.0.1:5000` para acceder a la página.

¡Listo! Ahora puedes utilizar el sistema de inicio de sesión en tu tienda online.
