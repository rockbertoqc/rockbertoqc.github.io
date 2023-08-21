¿Cuál es la diferencia entre las bases de datos SQL y las NoSQL?

Constantemente escuchamos los términos "base de datos SQL" y "base de datos NoSQL", pero, ¿sabes cuál es su principal diferencia?

Una base de datos SQL es aquella base datos relacional que está escrita en lenguaje SQL, es decir, una base de datos que está conformada por tablas que tienen filas (registros) y columnas (campos). La información de una base de datos SQL está almacenada de forma estructurada. 

Por otra parte, una base de datos NoSQL (también llamada no relacional) alberga información no estructurada y está diseñada para modelos de datos específicos que requieren esquemas flexibles. A diferencia de las bases de datos SQL, en la que las relaciones se definen mediante claves primarias, la flexibilidad de las bases de datos NoSQL permiten un desarrollo más rápido e iterativo. 

Para entender mejor, vayamos con un ejemplo.

Supongamos que tenemos una tabla llamada "computer_models" en una base de datos SQL que almacena información sobre modelos de computadora en venta. La información se almacenaría de esta forma en una base de datos SQL. 

```sql
-- Crear la tabla
CREATE TABLE computer_models (
    id INT PRIMARY KEY,
    nombre VARCHAR(50),
    marca VARCHAR(50),
    precio DECIMAL(10, 2),
    tipo_procesador VARCHAR(50),
    ram_gb INT,
    almacenamiento_gb INT
);

-- Insertar datos en la tabla
INSERT INTO computer_models (id, nombre, marca, precio, tipo_procesador, ram_gb, almacenamiento_gb)
VALUES
    (1, 'Modelo A', 'Fabricante1', 800, 'Intel i5', 8, 256),
    (2, 'Modelo B', 'Fabricante2', 1200, 'AMD Ryzen 7', 16, 512),
    (3, 'Modelo C', 'Fabricante1', 1500, 'Intel i7', 16, 1024);
```

Con este código, construiríamos una tabla así:

![Base de datos SQL](https://i.ibb.co/1fxDMMv/base-sql.png)

En cambio, si quisiéramos hacer esta base de datos en NoSQL (en este ejemplo usaremos MongoDB), el código sería estructurado de esta forma:

```json
[
  {
    "_id": 1,
    "nombre": "Modelo A",
    "marca": "Fabricante1",
    "precio": 800,
    "tipo_procesador": "Intel i5",
    "ram_gb": 8,
    "almacenamiento_gb": 256
  },
  {
    "_id": 2,
    "nombre": "Modelo B",
    "marca": "Fabricante2",
    "precio": 1200,
    "tipo_procesador": "AMD Ryzen 7",
    "ram_gb": 16,
    "almacenamiento_gb": 512
  },
  {
    "_id": 3,
    "nombre": "Modelo C",
    "marca": "Fabricante1",
    "precio": 1500,
    "tipo_procesador": "Intel i7",
    "ram_gb": 16,
    "almacenamiento_gb": "1TB"
  }
]
```

La elección de una base de datos depende de las necesidades que tengas para su uso. En este caso, una base de datos NoSQL podría resultarte útil en algunos aspectos:

a) Es flexible. En una base de datos NoSQL, no estás limitado por una estructura de tabla rígida. Puedes almacenar objetos JSON con estructuras flexibles. Esto podría ser útil si en el futuro deseas agregar campos adicionales específicos de ciertos modelos de computadora sin tener que alterar la estructura de la base de datos.
b) Datos anidados. En una base de datos NoSQL, puedes almacenar datos anidados dentro de un mismo documento. Esto es útil si quieres agrupar información relacionada, como detalles sobre la marca, especificaciones técnicas, u otros en un mismo documento, a diferencia de SQL, en donde requerirías hacer otra tabla estructurada. 
c) Escalabilidad horizontal. Si tienes un alto volumen de datos o un tráfico muy elevado en tu app, lo mejor es una base de datos NoSQL, pues está diseñada para agregar clústeres distribuidos de hardware para el manejo de cargas crecientes en lugar de escalar usando servidores caros. 
d) Es más fácil hacer consultas complejas y rápidas, debido a que su indexación y búsqueda está optimizada para búsquedas flexibles.

Si quieres ahondar más en modelos de bases de datos no relacionales, te recomiendo [dar clic en este enlace](https://aws.amazon.com/es/nosql/). 

¡Espero haberte ayudado un poco, desarrollador, desarrolladora!




