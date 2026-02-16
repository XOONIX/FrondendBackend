Base de datos relacionales, son aquellas que **Dependen** de otros valores para poder funcionar correctamente, ejemplo.

Estudiante Sena,--depende--centro institucional--Que a su vez depende-- De otras entidades..."Se organizan atravez de tablas que a su ves contienen columnas y relaciones"



Base de dato no-relacional, Son aquellas que no dependen de otros elementos, es decir, es un sistema de almacenamiento de información que no utiliza tablas, filas ni columnas para organizar los datos. "Suele darse para sistemas de información muy grande"



**Programación orientada a objetos**



Los objetos pasan a ser:



La Clase se convierte en una Tabla.

Los Atributos (propiedades) se convierten en Columnas.

Una Instancia (el objeto específico) se convierte en una Fila o Registro.

El Identificador (ID) del objeto se convierte en la Primary Key (PK).


¿QUÉ ES UNA BASE DE DATOS?

Es un conjunto organizado de datos que se almacenan de forma estructurada para **facilitar su acceso, gestión y actualización** mediante sistemas informáticos.

¿PARA QUÉ SIRVE UNA BASE DE DATOS?

* Almacenar grandes volúmenes de información
* Consultar datos de forma rápida
* Actualizar información fácilmente
* Evitar duplicación de datos
* Garantizar seguridad y respaldo de la información


COMPONENTES DE UNA BASE DE DATOS

*Datos**: información almacenada
*Tablas**: estructuras donde se guardan los datos
*Campos (columnas)**: tipo de información (nombre, edad, etc.)
*Registros (filas)**: conjunto de datos de una entidad
*Clave primaria**: identifica un registro de forma única
*Clave foránea**: conecta tablas entre sí
*Índices**: aceleran las búsquedas

Según su uso

*Locales**: en un solo equipo
*Distribuidas**: en varios servidores
*En la nube**: accesibles por internet
*Transaccionales**: operaciones diarias
*Analíticas (Data Warehouse)**: análisis y reportes

Comandos comunes 

 SQL (Structured Query Language)

*SELECT** → consultar datos
*INSERT** → insertar datos
*UPDATE** → actualizar datos
*DELETE** → eliminar datos




Llaves (Keys) y Funciones
Las llaves son las que permiten identificar y conectar la información.
Tipo de Llave
Función
Primary Key (PK)
Identificador único de un registro (ej. ID de usuario). No puede repetirse ni ser nulo.
Foreign Key (FK)
Una llave que referencia a una PK en otra tabla para crear un vínculo.
Composite Key
Combinación de dos o más columnas que juntas forman un identificador único.

Funciones Principales: Las bases de datos permiten realizar operaciones CRUD (Create, Read, Update, Delete) y funciones de agregación como SUM(), AVG() y COUNT().

Restricciones (Constraints)
Son reglas que aseguran la integridad de los datos. Si una operación no cumple la regla, la base de datos la rechaza.
NOT NULL: Asegura que una columna no quede vacía.
UNIQUE: Garantiza que todos los valores en una columna sean diferentes.
CHECK: Valida que el dato cumpla una condición (ej. edad > 18).
DEFAULT: Asigna un valor automático si no se provee uno.

Modelos y Clases
Existen dos grandes familias según la estructura:
Relacionales (SQL): Datos estructurados en tablas (filas y columnas). Ideales para transacciones seguras.
No Relacionales (NoSQL): Datos sin un esquema fijo. Pueden ser:
Documentales: (JSON/BSON).
Clave-Valor: Muy rápidos para caché.
Grafos: Para conexiones complejas (redes sociales).

Relaciones y Tipos
Definen cómo interactúa una entidad con otra:
1:1 (Uno a Uno): Un ciudadano tiene un solo pasaporte.
1:N (Uno a Muchos): Un cliente puede tener muchos pedidos.
N:M (Muchos a Muchos): Muchos estudiantes pueden inscribirse en muchos cursos (requiere una tabla intermedia).

Lenguajes y Ecosistema
Para dominar las bases de datos, estos son los nombres que debes conocer:
Lenguaje Estándar: SQL (Structured Query Language).
Gestores Populares (RDBMS): MySQL, PostgreSQL, SQL Server, Oracle.
Gestores NoSQL: MongoDB, Redis, Cassandra.
Concepto Clave: ACID: Un conjunto de propiedades (Atomicidad, Consistencia, Aislamiento y Durabilidad) que garantizan que las transacciones sean fiables.

Valor Añadido para tu Aprendizaje
Normalización: Es el proceso de organizar los datos para evitar la redundancia (no repetir información innecesariamente).
Índices: Son estructuras que mejoran la velocidad de búsqueda, como el índice de un libro





