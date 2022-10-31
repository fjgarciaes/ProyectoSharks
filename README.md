# ProyectoSharks

https://cdn.mos.cms.futurecdn.net/ZhiCPJJVnexUpJY7oYMeKF.jpg


En primer lugar importamos las librerias necesarias.

Cargamos el Dataframe.

Cambio los nombres de las columnas a minúscula y quito los espacios.

Vemos las dimensiones del Df así como la información del mismo.

Vemos los valores nulos que hay en cada columna y sacamos el porcentaje de nulos por columna así como un mapa de calor.

Elimino las columnas unnamed:22 y unnamed23, el resto de columnas con valores nulos por encima del 80% se mantienen ya que sus datos son relevantes.

Basandome en la columna Date elimino las filas en las que sus valores son nulos dejando el DataFrame con 6302 filas y 22 columnas frente a las 25723 filas y 24 columnas del Dataframe original 

Reemplazo el resto de valores nulos por unknown

En la columna name reemplazo los valores male y female por John Doe y Jane Doe para indicar que no se conoce su nombre 

Convierto la columna caseNumber en el id de los casos

Se limpia la columna date para que todas las fechas queden en formato año/mes/dia

Modifico el nombre de la columna country por country/aprox zone ya que los valores dentro de la misma no son únicamente países, para normalizarla se ponen todos sus valores en mayusculas y se sobreescribe el nombre de aquellos que contenían mas información.

Para la columna fatal(y/n) se cambia su nombre a fatal(y/n) & N/A se normalizan sus datos incluyéndolos todos en Y,N N/A y unknown 

Se realiza el mismo proceso para la columna sex, agrupando todos los valores entre F,M y unknown 

Para la columna type introduzco los valores boat y boating dentro de boating.

En la columna Age se cambian los valores introduciendo valores numéricos en lugar de strings considerando por ejemplo que la edad media de los teens es 15.5 años y así se procede con el resto.

En la columna activity se buscan valores usando regex y se simplifican a 17 tipos de actividades, dejando aquellos que no quedan claro en other.

Para la columna year reemplazamos los unknown por 0.0 y se eliminan los ceros que tenian al final.

Se comprueba que todos los tipos de datos de las distintas columnas son correctos, ademas los float se cambian a float32, los integer a int16 y los object a category para reducir su uso de memoria.

Para finalizar se realizan una serie de cross tables para poder sacar conclusiones.
Las conclusiones que observo son las siguientes:
- De las actividades de las que se tienen datos el mayor numero de ataques se producen pescando o nadando.
- El mayor numero de ataques los recibe el sexo masculino.
- La gran mayoria de los ataques no fueron letales.
-Los paises en los que se tienen mas registros de ataques son Estados unidos y Australia.
- Por último se observa que el mayor numero de ataques registrados son del año 2015.
