# consultas_1_sql
#  Introduccion a las consultas a una BD usando SQL

## Base de Datos: Ventas
## Tabla Cliente

![Tabla Cliente](tabla_cliente.png "Tabla Cliente")

## Instruccion SELECT
- Permite seleccionar datos de un tabla.
- Su formato es: `SELECT campos_tabla FROM nombre_tabla`

### Consulta No. 1
1. Para visualizar toda la informacion que tiene la tabla Cliente se puede incluir con la instruccion SELECT el caracter **\*** o cada uno de los campos de la tabla

- `SELECT * FROM Cliente`
![Consulta 1-1](consulta1_1.png "Consulta 1-1")

- `SELECT identificacion, nombre, apellido, direccion, telefono, ciudad_nac, fecha_nac FROM Cliente`

![Consulta 1-2](consulta1_2.png "Consulta 1-2")


### Consulta No. 2

2. Para visualizar solamente la identificación del Cliente: `SELECT identificacion FROM Cliente`

![Consulta 2-1](consulta2_1.png "Consulta 2-1")

### Consulta No. 3
3. Si se desea obtener los registros cuya identificacion sea mayor o igual a 150, se debe utiliza la clásula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELECT * from Cliente WHERE identificacion>=150`


![Consulta 3](consulta3.png "Consulta 3")

###  Consulta No. 4
4. Se desea obtener los registros cuyos apellidos sean Vanega o Cetina, se debe utulizar el operador `IN` que especifica los registros que se quieren  visualizar de una tabla.

`SELECT apellidos, nombre from Cliente  WHERE apellidos IN('Vanega', 'Cetina')`

![Consulta 4-1](consulta4_1.png "Consulta 4-1")


O se puede utilizar el operador OR

`SELECT apellidos, nombre from Clientes WHERE apellidos= 'Vanega' OR apellidos='Cetina'`

![Consulta 4-2](consulta4_2.png "Consulta 4-2")



###  Consulta No. 5
5. Se desea obtener los registros cuya identificación sea menor de 110 y la ciudad sea Cali, se debe utilizar el operador `AND`

`SELECT * from Cliente WHERE identificacion<=120 AND ciudad='Cali`

![Consulta 5](consulta5.png "Consulta 5")


###  Consulta No. 6
6. Si se desea obtener los registros cuyos nombres empiezen por la letra 'A', se debe utilizar el operador `LIKE` que utiliza los patrones `%` (todos) y `_` (caracter).

`SELECT from Cliente WHERE nombre LIKE 'A%'`

![Consulta 6](consulta6.png "Consulta 6")

###  Consulta No. 7
6. Se desea obtener los reigstros cuyos nombres contengan la letra 'a'


`SELECT * from Cliente WHERE nombre LIKE '%a%'`

![Consulta 7](consulta7.png "Consulta 7")

### Consulta No. 8

8. Se desea obtenere los registros donde la cuarta letra del nombre del cliente seala letra 'a'.

`SELECT * from Cliente WHERE nombre LIKE '___a%'`

![Consulta 8](consulta8.png "Consulta 8")


### Consulta No. 9

9. Si se desea obtener los registros cuya identificacion  esté entre el intervalo 110 y 150, se debe utilizar la cláusula 'BETWEEN', que sirve para especificar un intervalo de valores.

`SELECT * from Cliente WHERE identificacion BETWEEN 110 AND 150`

![Consulta 9](consulta9.png "Consulta 9")
