## Tarea #1

#### Fernando Morales B85338

1. Las siguientes tres preguntas serán las estudiadas con el dataset [*Obesity among adults by country, 1975-2016*](https://www.kaggle.com/amanarora/obesity-among-adults-by-country-19752016?select=data.csv):
    - Cuál es el país cuyo índice de obesidad ha aumentado porcentualmente más desde el 2006 hasta el 2016?
    - Cuál es el país con el índice promedio de obesidad menor entre 2006 hasta el 2016?
    - Cuál sexo es el que promedia un índice mayor de obesidad?

2. Los problemas que tiene el dataset son los siguientes:
   - Tiene como columnas los valores de los años
      - *OpenRefine* tiene una función que permite establecer estos valores y pasarlos a celdas
   - No existe una columna para los sexos
     - Existe una fila que nos permite identificar cuándo se está hablando de sexo femenino, masculino o ambos
   - Los índices de obesidad junto con sus intervalos correspondientes están ubicados en la misma celda
     - Se debe separar ambos valores en diferentes columnas, ya que nos es útil el promedio de los índices, no necesariamente los intervalos
   - La columna de países no está correctamente puesta
     - Se debe cambiar el nombre de la columna por "Países" 
   - Las primeras dos filas del dataset realmente no aportan ninguna información
     - Al cargar el *dataset* en OpenRefine, existe la opción de omitir una cantidad definida de líneas, por lo que se debe eliminar las primeras 3 filas 

3. Los atributos que son absolutamente necesarios para responder las preguntas son los siguientes: 

   - **País**: este atributo permitiría poder responder la primer pregunta al clasificar los índices correspondientes por país
   - **Año**: este atributo es clave, ya que queremos solo considerar los valores que se encuentren entre 2016 y 2006, para poder crear una visualización de una década exacta
   - **Sexo**: este atributo permitiría poder corrresponder los diferentes índices a cada uno de los sexos respectivos
   - **Indice de obesidad promedio**: este atributo es clave para las preguntas de investigación, ya que todo el *dataset* gira alrededor de este atributo  

4. En total, se aplicaron un total de 14 transformaciones, que pueden ser vistas en el archivo *`.json`* correspondiente. Lo siguiente es un resumen de estas transformaciones, con el objetivo de cada un de ellas:
    1. Inicialmente, al cargar el *dataset*, borramos las primeras tres filas, ya que no agregan información relevante. Al hacer esto, las columnas quedan con los valores de los años, con un 2 al final si son de sexo masculino, con un 3 al final si son de sexo femenino o únicamente el año si abarca ambos sexos.
    2. Se renombra la columna de países a `Country`.
    3. Se utiliza el comando de *`Transpose cells across columns into rows`*, el cual permite convertir los nombres de las columnas en valores para cada una de las filas, lo que genera una de `Year`, que contiene los años que estaban como columnas, y otra columna `Index`, que contiene todos los valores de los índices correspondientes.
    4. Se separa la columna "Año" por la longitud de la celda, donde los primeros 4 caracteres determinan el año correcto, mientras que el último caracter `(vacío, 2 o 3)` determina el sexo de la fila correspondiente, lo que genera dos filas llamadas "Year 1" y "Year 2"
    5. La primera columna `Year 1` se renombra a `Year`
    6. En la segunda columna `Year 2`, se aplica una transformación, en donde:
        - Si el valor de la celda es 2, el valor ahora va a ser `Male`, para representar al sexo masculino
        - Si el valor de la celda es 3, el valor ahora va a ser `Female`, para representar al sexo femenino
        - Si no cumple con ninguna de las condiciones anteriores, el valor ahora va a ser `Both`, para representar la combinación de los índices de ambos sexos
    7. La columna `Year 2` es renombrada a `Sex`, para representar el sexo correspondiente a los índices
    8. La columna `Index` es separada por el espacio vacío, para separar el valor promedio del índice y los intervalos.
    9. Se eliminan dos columnas extras generadas en el paso anterior.
    10. Se renombran las columnas generadas en el paso **8** a `Index Average` y `Index Intervals`.
    11. Se crea un *numeric facet* que filtra los años desde el 2005 o menores para así borrarlos del *dataset*, ya que no van a ser utilizados para las preguntas de investigación. Esta transformación resulta en **18135** filas borradas del *dataset*.
    12. Finalmente, se borran aquellos valores de índices que no existen. Para esto, se crea un *numeric facet* para la columna `Index Average`, la cual muestra **132** filas sin datos, las cuales son borradas del *dataset*.
**NOTA: si se desean replicar los resultados de las operaciones, se tienen que borrar las primeras 3 filas en OpenRefine** 
5. **Aclaraciones:** El *dataset* inicial tiene el nombre de `data.csv`, el *dataset* resultante tiene el nombre de `clean_data.csv` y el historial de operaciones tiene el nombre de `operation_history.json`.  