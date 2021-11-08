# Apuntes día 8 de noviembre

## Tema 3: *_SQL_*

SQL {structure querry language}

#### Conceptos generales

* Este lenguaje contiene relativamente pocas sentencias
* Las secuencias se forman for clausulas
* El lenguaje no entiende de mayusculas o minusculas.
    * Pero se usan mayusculas como buena practica
* Las secuencias se divide en líneas por clusulas para mantener estilo
* Las clausulas que daremos en clase son obligatorias

Las sentencias que veremos son:

* SELECT
* INSERT
* DELETE
* UPDATE

### Select

El select es equivalente a la proyección no a la selección

```SQL
SELECT * FROM CLIENTE
```

Esto muestra todas las tuplas de Cliente.

Aunque SELECT sea la proyección, esta proyección *no* borra los duplicados a no ser que se lo indiques; no es una proyección algebraica.

```SQL
SELECT NBC FROM CLIENTES
``` 
Para que no existan duplicados lo escribiriamos de la siguiente forma añadiendo la extension _DISTINCT_.

```SQL
SELECT DISTINCT NBC
FROM CLIENTES;
```

Si quiero proyectar sobre 2 columnas lo puedo especificar:

```SQL
SELECT DNI, NBC
FROM CLIENTES;
```

Lo que no podemos hacer es utilizar el elemento de seleccionar todos (*) junto con una columna. (`SELECT DNI, *`)

Para crear un alías para la selección que queremos hacer lo escribiremos de la siguiente manera:

```SQL
SELECT FF_FI "Número de días"
FROM PLAN_DOCENTE;
```
También se aceptaría como nombre _numero_de_dias_.