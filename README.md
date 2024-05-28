# <p align="center">Challenge AluraGeek</p>

## Objetivo del Desafío
En este desafío se desarrollará una aplicación para:
* listar productos
* registrar productos
* eliminar productos

## Servidor Local
Este proyecto incluye un servidor local configurado con JSON Server para simular una API REST, por lo cual es necesario descargarlo para probar su funcionamiento.

### Iniciar el Servidor Local

Requisitos:
 
* Node.js y npm 

Luego, se ejecuta el siguiente comando en la terminal:

    1. npm init

*Se puede ejecutar el comando `npm init -y` para no tener que ingresar los datos.*

---
    2. Crear archivo db.json:

        2.1. Crear una carpeta database
        2.2. Crear dentro de database un archivo db.json

            {
                "products": [
                     {
                        "id": "22f1",
                        "name": "consola manual",
                        "price": "100",
                        "image": "https://smartjoys.co/wp-content/uploads/2023/12/ConsolaR35S.jpg"
                        },
                ]
            }
---
    3. npm install json-server
Se crea el archivo **node_modules** y dentro del **package.json** se agrega la siguiente dependencia:

        "json-server": "^1.0.0-beta.0"
---
    4. npx json-server --watch db.json --port 3000

*Sin embargo, se puede modificar el package.json agregando en el campo scripts el siguiente script:*

            "start": "npx json-server --watch database/db.json --port 3000"

Con este cambio, simplemente se inicia el servidor JSON ejecutando:

           npm start

Esto iniciará el servidor local, permitiendo acceder a la API REST simulada en http://localhost:3000, y observará el archivo db.json en el puerto 3000 ruta products:

        http://localhost:3000/products

### Ejemplos usando la API REST
* GET http://localhost:3000/products: devuelve una lista de todos los productos disponibles.
* POST http://localhost:3000/products: para agregar un nuevo producto a la lista.
* DELETE http://localhost:3000/products/1: para eliminar el producto con el ID  de la lista, por ejemplo ID 1. 

## Informacion sobre el proyecto:
1. **db.json (database/db.json):** Tiene datos de productos en formato JSON que pueden ser consultados y modificados mediante solicitudes HTTP.

2. **main.js (js/controllers/main.js):** Tiene funciones que interactúan con la interfaz de usuario para mostrar la lista de productos y manejar eventos de usuario.

3. **customError.js (js/err/customError.js):** Tiene mensajes personalizados de errores que pueden ser utilizados en la validación de formularios .

4. **productServices.js (js/services/productServices.js):** Tiene funciones que interactúan con una API REST simulada para realizar operaciones relacionadas con productos, como obtener la lista de productos, agregar un nuevo producto y eliminar un producto existente.

    ### Métodos HTTP utilizados:
    * GET: para listar productos
    * POST: para registrar productos
    * DELETE: para eliminar productos


5. **formValidator.js (js/validators/formValidator.js):** Tiene la lógica para verificar la validez de los datos ingresados por el usuario en el formulario de registro de productos.

6. **index.html:** Tiene la estructura básica de la página web y enlaza con los archivos CSS y JavaScript necesarios para mostrar la lista de productos y proporcionar funcionalidad interactiva al usuario.


## Principales Tecnologías utilizadas
* HTML5
* CSS3
* JAVASCRIPT

## Tecnologías secundaria
* Node.js y npm (incluyendo node_modules)
* JSON Server (db.json para simular API)
* VsCode
* Git
* GitHub

## Herramientas de Gestión y Diseño
* **Trello:** herramienta de colaboración y gestión de proyectos.
* **Figma:**  se creo un modelo que muestra una representación visual del Alura Geek.
        
