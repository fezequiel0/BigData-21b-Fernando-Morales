# Reporte 7 | 28 de noviembre
### Fernando Morales B85338

Las últimas dos semanas hemos visto los siguientes temas:

- Análisis de flujo de datos
  - Su enfoque es en procesamiento y análisis de grandes volumenes de datos, los cuales:
    - Vienen en grandes cantidades
    - Cambian muy rápido en el tiempo
    - Necesitados para tomar decisiones rápidamente
  - Provee un sistema de procesamiento en timmpo real, sin necesariamente almacenar los datos
  - Estos flujos de datos no necesarimente constante, al igual que el tiempo de procesamiento
    - Esta es una de las características claves entre *streaming* y el procesamiento con una base de datos
  - Existen varios tipo de procesamiento:
    - *Bounded data*: son procesos más largos que no tienen que ejecutarse lo más rápido posible, ya que no son sujetos a análisis de datos en tiempo real
    - *Unbounded data*: lo opuesto a *bounded data*
      - *Batch*: lo más similiar a bounded data que hay, que son procesados cada cierto intervalos de tiempo
      - *Streaming*: no en orden, altamente variantes
        - *Time agnostic*: el tiempo es completamente irrelevante a la hora del procesamiento
        - *Approximation*: convierte los datos a algo simlar, esta transformación puede ser de cualquier forma
        - *Windowing*: partir los pedazos del *stream*
        - *Windowing by processing time*: toma bloques de cierta cantidad de tiempo para después procesarlos
        - *Windowing by event time*: toma bloques por ciertos eventos que ocurren, como puede ser una aplicación corriendo o similar
        - *Tumbling window*: se dispara el procesamiento cuando cierto tamaño de ventana se llena
  - Se pueden aplicar filtros al *stream* para poder agarrar observaciones que cumplan con ciertas características
  - Acá entra el *bloom filter*, el cual se encarga de reducir el tamaño de entrada del *stream*, solo permitiendo ciertas tuplas/hileras que cumplan ciertas condiciones
  - Hay varios tipos de procesos aplicables para reducir el tamaño del *stream*, que incluyen:
    - *Filtering*
    - *Enriching*: cambiar el *stream* para agregarle información previo a la etapa de análisis
    - *Aggregation*: aplicar diferentes operaciones sobre la información entrante
    - *Event detection*: detectar, dadas ciertas condiciones, si algo ocurrió en el *stream*
- Series de tiempo
  - En términos sencillos, es la visualización de un atributo a través de cierta medición de tiempo, sea meses, minutos, microsegundos, etc.
  - Su uso puede ser muy variado, pero es sobre todo utilizado para realizar pronósticos de ciertos eventos
  - Dentro de estas mismas, están las tendencias, temporalidades y el ruido, las cuales representan comportamientos o fluctuaciones de la variable de interés a través de la serie de tiempo
  - Lo que se quiere con las series de tiempo es poder identificar estos tres componentes, para así poder tener una mayor comprensión del comportamiento de la variable
    - Para lograr, esto existen técnicas para ir separando cada uno de los componentes como *moving average*, elmiminación de tendencia, eliminación de temporalidad, entre otros
  - Después de tener estas series de tiempo, se utilizan diferentes tipos de modelos de predicción, los cuales pueden ser:
    - *Exponential smoothing*: provee un estimado del promedio de valores de las observaciones hasta cierto tiempo t, el cual se va progresivamente mejorando y cambiando los parámetros para poder entender de la mejor manera la forma en que se comporta la variable en cuestión
    - *Auto-regressive*: dependiendo de la forma de los datos y los coeficientes, el uso del tipo de este modelo puede ir cambiando.
    - *Machine learning*

Sobre todo la materia del análisis de flujo de datos me llamó la atención, ya que en el curso de `Investigación en Ciencias de la Computación` estamos usando esta técnica, sin siquiera saber que la estábamos aplicando. 

Por el momento, no siento que tenga alguna duda sobre la materia estudiada; es cuestión de poner en práctica lo aprendido a través de las tareas y las prácticas, las cuales definitivamente han ayudado bastante para la comprensión de los temas de la clase.

Tal vez la materia de series de tiempo sea un poco difícil de visualizar cómo la utilizaría, pero siento que el análisis de flujo de datos es muy probable que tenga que usarlo de alguna forma u otra; incluso no tiene que ser profesionalmente. Ya que cada vez todo genera una enorme cantidad de datos en tiempo real, es muy realista y posible que este contenido sea muy útil en el futuro.

Por el momento, no he utilizado ningún material extra; las prácticas y las presentaciones vistas en clase son más que suficientes para entender el funcionamiento de los modelos explicados y las técnicas vistas.