# Reporte 3 | 3 de octubre
### Fernando Morales B85338

Las últimas dos semanas hemos visto los siguientes temas:

- Las diferentes características que tienen los modelos y los posibles tipos que los conforman:
  - Modelos lineales contra modelos no lineales
  - Modelos de tipo *caja negra*, donde no se entiende realmente el funcionamiento o el razonamiento del modelo, a pesar de que son extremadamente efectivos, contra modelos descriptivos, donde se puede explicar fácilmente el razonamiento tras las decisiones, aunque no puede ser mejor que los modelos de tipo *caja negra*. 
  - Modelos de tipo *first principle*, donde normalmente se tiene un cálculo exacto o basado en cierto conocimiento (por ejemplo, la derivada de 3x con respecto a x es 3) contra modelos *data driven*, los cuales son basados en correlaciones observadas entre variables de entrada contra las variables de salida.
  - Modelos de tipo estocástico, donde son determinados en función de una probabilidad o "aleatoriamente", contra modelos de tipo determinístico, los cuales, dado cierto valor de entrada, siempre producirá el mismo valor de salida, lo cual lo hace exacto
  - Modelos planos, donde se depende de ciertos mismos tipo de variables, contra modelos con jerarquías, donde son altamente complejos y toma diferentes tipos de variables y propiedades, los cuales son usados para resolver problemas con varios niveles de complejidad.
- La evaluación de los modelos en sí:
  - Partición del data-set total en 60% para entrenamiento, 20% para validación y 20% para evaluar el modelo en sí
  - Existen diferentes métricas para evaluar un modelo, las cuales pueden ser binarias, multiclase o con valores específicos
- Arboles de decisión
  - Es un tipo de modelo que clasifica según su profundidad y una cantidad de características establecidas
  - Por ejemplo, para clasificar animales, una característica puede ser que si ponen huevos o no; si pone huevos, es un ovíparo y si no, es un mamífero. Entonces, si se tiene una muestra donde el animal no pone huevos, a través del árbol de decisión, se puede clasficiar como mamífero. 
  - Las diferentes características pueden ser más importantes que otras o más relevantes a la hora de clasificar las muestras, como lo podría ser para el caso de dar ciertos préstamos.
- Existen varios tipos de estrategias de entrenamiento, cada una con sus ventajas y desventajas
- Para saber cuál estrategia de entrenamiento es la ideal para el modelo que se tiene, se tiene que primero conocer muy bien el *dataset* que se esté utilizando (EDA).
- Pudimos ver cómo, al cambiar la forma de validación y entrenamiento del modelo, puede terminar resultando en modelos completamente distintos, donde unos terminan siendo óptimos bajo ciertas circunstancias. 

Siento que esta materia ha sido demasiado importante para poder entender el funcionamiento de los modelos en general y cómo definitivamente cada situación amerita tipos diferentes de modelado, de entrenamiento y de evaluación de este. Con esto entendido, creo que puedo visualizar mucho mejor cómo los modelos funcionan y de ser el caso, escoger el correcto cuando sea el momento.

Por el momento, no siento que tenga alguna duda sobre la materia estudiada; es cuestión de poner en práctica lo aprendido a través de las tareas y las prácticas, las cuales definitivamente han ayudado bastante para la comprensión de los temas de la clase.

Los fundamentos de los árboles de decisión definitivamente van a ser utilizados en mi vida profesional, ya que se extiende del análisis de grandes volúmenes de datos, ya que son demasiado útiles para la clasificación de cualquier tipo de objeto y son relativamente sencillos de implementar. 

Por el momento, no he utilizado ningún material extra; las prácticas y las presentaciones vistas en clase son más que suficientes para entender el funcionamiento de los modelos explicados y las técnicas vistas.