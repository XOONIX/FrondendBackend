Que es SQL --> Structure Query Language

y esta compuesto por dos partes DML y DDL

DML-->Data Manupulation Language

DDL-->Data Defitive Language

---



**Hacer una infografía sobre:**

SQL es el lenguaje estándar para comunicarse con Sistemas de Gestión de Bases de Datos Relacionales (RDBMS).



**1. Desglose Etimológico y Conceptual**

**Structured (Estructurado):** Los datos se organizan en tablas con filas y columnas predefinidas, lo que permite un orden lógico y relaciones claras entre diferentes conjuntos de datos.



**Query (Consulta):** La función principal es realizar preguntas complejas a la base de datos para extraer exactamente la información necesaria.



**Language (Lenguaje):** Posee su propia sintaxis, gramática y reglas que permiten a los humanos dar instrucciones precisas que las computadoras pueden procesar.

---



**2. Los 5 Sublenguajes de SQL**

SQL no es un solo bloque de comandos; se divide en subconjuntos especializados según la tarea



**1. DDL (Data Definition Language)**

Se usa para definir, modificar o eliminar la estructura de los objetos de la base de datos (tablas, índices, etc.).

CREATE: Para crear una nueva tabla o base de datos.

ALTER: Para modificar la estructura de una tabla existente (ej. añadir una columna).

DROP: Para eliminar permanentemente una tabla o base de datos.

TRUNCATE: Se utiliza para eliminar todos los registros de una tabla de forma rápida. A diferencia de DELETE (que es DML), TRUNCATE reinicia los contadores de identidad (como los ID autoincrementables) y no procesa fila por fila, por lo que es mucho más eficiente para vaciar tablas grandes.

RENAME: Permite cambiar el nombre de un objeto de la base de datos, como una tabla o una columna, sin necesidad de borrarla y volverla a crear.

COMMENT: Se emplea para añadir comentarios explicativos al diccionario de datos sobre una tabla o columna, lo cual es útil para la documentación interna del esquema.

**2. DML (Data Manipulation Language)**

Permite manipular los datos que ya existen dentro de las tablas.

INSERT: Para añadir nuevas filas de datos a una tabla.

UPDATE: Para modificar valores en registros existentes.

DELETE: Para eliminar filas específicas de una tabla.

**3. DQL (Data Query Language)**

Se enfoca exclusivamente en la recuperación y consulta de información sin alterarla.

SELECT: El comando principal para extraer datos.

SELECT DISTINCT: Para obtener valores únicos eliminando duplicados.

SELECT ... ORDER BY: Para recuperar datos organizados de forma ascendente o descendente.

**4. DCL (Data Control Language)**

Utilizado para gestionar la seguridad y los permisos de acceso a los datos.

GRANT: Para dar permisos de acceso a un usuario.

REVOKE: Para quitar permisos previamente otorgados.

DENY: Para prohibir explícitamente un permiso a un usuario (común en SQL Server).

**5. TCL (Transaction Control Language)**

Gestiona los cambios realizados por las sentencias DML para asegurar que las transacciones sean estables.

COMMIT: Para guardar permanentemente todos los cambios de la transacción actual.

ROLLBACK: Para deshacer los cambios si ocurre un error antes de finalizar la transacción.

SAVEPOINT: Para establecer un punto de retorno temporal dentro de una transacción larga.



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



**Categoría 			Siglas		Función Principal								Comandos Clave**



Definición de Datos		DDL	Define la estructura: crear, modificar o borrar tablas y bases de datos.		CREATE, ALTER, DROP, TRUNCATE

Manipulación de Datos		DML	Permite trabajar con el contenido: insertar, actualizar o borrar registros.		INSERT, UPDATE, DELETE

Consulta de Datos		DQL	El más usado. Se enfoca exclusivamente en la recuperación de información.		SELECT

Control de Datos		DCL	Gestiona la seguridad y los permisos de acceso de los usuarios.				GRANT, REVOKE

Control de Transacciones	TCL	Administra cambios permanentes y asegura la integridad de las operaciones.		COMMIT, ROLLBACK, SAVEPOINT

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_



**3. Características Fundamentales**

**Declarativo:** Tú le dices a SQL qué quieres obtener, no cómo debe hacerlo paso a paso.

**Propiedades ACID:** Garantiza que las transacciones sean Atómicas, Consistentes, Aisladas y Duraderas, lo que previene la pérdida o corrupción de datos.

**Independencia del Software:** Aunque existen variantes (como MySQL o PostgreSQL), el núcleo de SQL es un estándar internacional (ANSI/ISO).



---



**4.** **ACID:** son un acrónimo que representa las cuatro propiedades fundamentales que garantizan que las transacciones en una base de datos se realicen de forma fiable y segura. Una transacción es un conjunto de operaciones (como transferir dinero de una cuenta a otra) que debe ejecutarse como una sola unidad.



**A - Atomicidad (Atomicity):** La transacción es una unidad indivisible; se realiza todo o nada. Si un solo paso de la operación falla, se deshacen todos los cambios realizados hasta ese momento (rollback), regresando la base de datos a su estado original.

**C - Consistencia (Consistency):** Garantiza que una transacción solo lleve a la base de datos de un estado válido a otro estado válido. Se deben respetar todas las reglas y restricciones (como que un saldo no sea negativo) antes y después de la operación.

**I - Aislamiento (Isolation):** Asegura que las operaciones realizadas por transacciones simultáneas no interfieran entre sí. Cada transacción debe ejecutarse como si fuera la única en el sistema, haciendo que sus estados intermedios sean invisibles para las demás hasta que finalicen.

**D - Durabilidad (Durability):** Una vez que la transacción se ha completado con éxito, los cambios son permanentes y no se perderán, incluso si ocurre un fallo del sistema, un corte de energía o un error de hardware inmediatamente después.



---

**5. Tipos de SQL según el Motor (Dialectos)**

Aunque existe un estándar (ANSI SQL), cada empresa ha creado su propia "versión" o dialecto con funciones extras:



**MySQL:** El más popular para aplicaciones web y de código abierto.

**PostgreSQL:** Conocido por ser el más avanzado y fiel al estándar.

**SQLite:** Una versión ligera que no requiere servidor, ideal para apps móviles.

**T-SQL** **(Transact-SQL):** La variante utilizada por Microsoft SQL Server.

**PL/SQL:** La extensión procedimental utilizada por Oracle Database.





**MySQL**

Ideal para: Web, WordPress y tiendas online.

Lo mejor: Es extremadamente rápido leyendo datos y muy fácil de aprender.

Lo peor: Carece de algunas funciones de análisis avanzado.

Arquitectura: Requiere instalación de servidor.

**PostgreSQL**

Ideal para: Inteligencia Artificial, apps financieras y datos geográficos.

Lo mejor: Es el más potente; maneja datos complejos (JSON, mapas, vectores) con precisión absoluta.

Lo peor: Puede ser más pesado de configurar y un poco más lento en tareas muy simples.

Arquitectura: Objeto-relacional (servidor).

**SQLite**

Ideal para: Apps de celular (Android/iOS) y pruebas rápidas.

Lo mejor: No se instala; es solo un archivo que puedes llevar en un USB.

Lo peor: Se bloquea si muchos usuarios intentan escribir datos al mismo tiempo.

Arquitectura: Sin servidor (vive dentro de tu aplicación).



**Dialectos de Programación (Extensiones)**

T-SQL y PL/SQL no son motores independientes, sino los lenguajes de programación de los gigantes corporativos:

**T-SQL**: El lenguaje de Microsoft SQL Server. Optimizado para integración con el ecosistema Windows.

**PL/SQL**: El lenguaje de Oracle. Diseñado para lógica empresarial masiva y máxima seguridad.



\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

## 

## Apuntes



Pasos para crear una base  de datos:



Primero se crea la base de datos "CREATE DATABASE"+ nombre

"CREATE TABLE" + nombre + (

Segundo se crea la tabla "Nombre de la tabla" + "Tipo de dato (int, char…)

Segundo opcional, se crea un auto-incrementador "IDENTITY(1,1)"

Tercero se agrega la llave primaria "PRIMARY KEY"

Cuarto creación de atributos "Nombre + tipo de valor"

Quinto, se agrega obligatorio o no obligatorio "NULL o NOT NULL



Una llave primaria nunca puede ser "NULL" es decir siempre es obligatoria.

"ADD" es para añadir una columna

"BIT" funciona como boleano

"DEFAULT" dato por defecto



Para modificar la tabla en caso de un error se usa "ALTER TABLE" + nombre

En la siguiente linea usamos "ADD" + nombre + TipodeDAto + "Null o Not null"



Borrar, es limbpiar una tabla, es decir dejar vacía

Borrado lógico, 1 para activo 0 para no activo

Eliminar, es eliminar por completo de la base de datos

