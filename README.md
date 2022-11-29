# ProyectoSharks

![ZhiCPJJVnexUpJY7oYMeKF](https://user-images.githubusercontent.com/114060666/199090896-e12f8be1-db34-49a2-a696-d6f6c68b1273.jpg)

OBJETIVO:

Limpiar el máximo posible de la base de datos.

Restricciones:

Solo se pueden eliminar las columnas que tengan mas de un 80% de nulos

Debemos finalizar la limpieza con mas de 6000 filas.

EXPLORACIÓN DE LA BASE DE DATOS:

- Importación y lectura del archivo.

- Conversión a dataframe.

- Observación de tipos de variables, duplicados, valores nulos y cantidad de registros.

PRIMEROS PASOS PARA LA LIMPIEZA:

1) Adaptar los nombres de columnas,quitando espacios y convirtiendo todo a minuscula.

2) Eliminación de 2 columnas con mas del 80% de nulos.
En primer lugar importamos las librerias necesarias.

3) Eliminación de filas con muchos valores nulos.

4) Rellenar el resto de valores nulos con unknown.

PROCESO DE LIMPIEZA:

- La columna casenumber se convierte en el id de los casos.

- En la columna name se reemplazan los valores desconocidos por John Doe o Jane Doe en función del sexo.

- Para la columna date se cambia el formato para conseguir que queden todos los datos con año/mes/dia 

- Se modifica el nombre de la columna country y se normaliza dejando todo sus valores en mayusculas y sobrescribiendo aquellos datos que lo necesitan.

- En la columna fatal se modifica su nombre y se normalizan los datos.

- En la columna sex se sigue el mimso proceso que se utilizo para la columna fatal

- En la columna type se normalizan todos los valores

- Se modifica la columna age para que sus valores sean numericos.

- En la columna activity se utiliza regex para quedarme unicamente con 17 tipos de actividades

- Se igualan las columnas que aportan la misma información ya que no se pueden eliminar.

- Se reemplazan los valores desconocidos de la columna year por valores numericos

- Se cambia el tipo de dato de todas las columnas para reducir el uso de memoria




Para finalizar se realizan una serie de cross tables para poder sacar conclusiones.
Las conclusiones que observo son las siguientes:
- De las actividades de las que se tienen datos el mayor numero de ataques se producen pescando o nadando.
- El mayor numero de ataques los recibe el sexo masculino.
- La gran mayoria de los ataques no fueron letales.
- Los paises en los que se tienen mas registros de ataques son Estados unidos y Australia.
- Por último se observa que el mayor numero de ataques registrados son del año 2015.
