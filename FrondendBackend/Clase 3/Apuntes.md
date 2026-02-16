Clase 3 16/02/2026



**Programación orientada a objetos**



Los objetos pasan a ser:



La Clase se convierte en una Tabla.

Los Atributos (propiedades) se convierten en Columnas.

Una Instancia (el objeto específico) se convierte en una Fila o Registro.

El Identificador (ID) del objeto se convierte en la Primary Key (PK).



**Normalización**

Se divide en 6 normas principales, pero se considera normalizada una base de datos al cumplir almenos 3 primeras



-1NF. Que los atributos sean bien divisibles

-2NF. Toda la información depende de la llave primaria "La llave primaria es único he irrepetible"
      (Llave simple, esta formada por un solo campo. Llave compuesta tiene dos o mas campos.)

-3NF. Si una base de dato cumple las dos primeras inmediatamente cumple la 3



**Relaciones y Tipos**

Definen cómo interactúa una entidad con otra:

1:1 (Uno a Uno): Un ciudadano tiene un solo pasaporte.

1:N (Uno a Muchos): Un cliente puede tener muchos pedidos.

N:M (Muchos a Muchos): Muchos estudiantes pueden inscribirse en muchos cursos (requiere una tabla intermedia).



**Transformación de MER a "Modelo relacional"**

Es una serie de pasos para transformar o adaptar el diagrama MER al Modelo relacional.



**Restricciones (Constraints)**

Son reglas que aseguran la integridad de los datos. Si una operación no cumple la regla, la base de datos la rechaza.

**NOT NULL:** Asegura que una columna no quede vacía.

**UNIQUE:** Garantiza que todos los valores en una columna sean diferentes.

**CHECK:** Valida que el dato cumpla una condición (ej. edad > 18).

**DEFAULT:** Asigna un valor automático si no se provee uno.



-----------------------------------------------------------------------------------------------------------------------



|                                   SENA |Entidad|
|-|-|
|PROGRAMA|Atributo|
|FICHA: -> Numérico |Atributo|
|CENTRO|Atributo|
|REGIONAL|Atributo|
|JORNADA|Atributo|



Una entidad es una clase en base de datos, esta compuesta por atributos...



Tipos de datos: 

int: Para valores numéricos operacionales 

varchar: Es el equivalente a un "string" pero en base de datos.

decimal: Sobre todo es para valores monetarios (solo separador decimal) 

bit: Es el equivalente a un dato boolean (true"1", false"0") 

float: Permite un numero racional demasiado grande (separador de mil y demás)

date: Solo almacena fecha

datetime: Almacena fecha y hora

bigint: El mismo "int" pero de 64 bites, es decir soporta mas valores. 

Uniqueidentifier --> Guid 





Se agrega un valor "int" solo cuando se va a operar con el valor. Ejemplo "La cedula no seria un valor int, porque no se van a realizar operaciones con el" 



-----------------------------------------------------------------------------------------------------------------------------------------------------------

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

|No. Factura | Tipo Documento | No. Documento | ProductoID | ValorUnitario | Cantidad | VrTotal|                         Entidades: Factura, TipoDocumento, Producto

|------------|----------------|---------------|------------|---------------|----------|--------|                         1-Cedula- CC    2-Cedula-CE.....

|114-->Var(8)|       1 -->Int |12345-->Var(10)| 1234-->    |1.00,0->decimal| 9-->float|  6-->  |                         Las llaves foraneas, tienen el mismo tipo de

|llave primar| llave foranea  |               | Dpende (PK)|               |          |Decimal |                         dato que las "PK"

| (PK)       | (FK)           |               |            |               |          |        |                         Los datos Varchar obligatoriamente debe tener 

&nbsp;                                                                                                                        una longitud maxima









Cuando varchar no alcanza la cantidad de digitos especificada llena con espacios 



































&nbsp;





