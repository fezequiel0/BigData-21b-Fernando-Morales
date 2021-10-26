## How to Choose an Activation Function for Deep Learning

En este tutorial, se vieron los siguientes temas:

- `Activation Functions`
  - Permiten generar cierto valor de salida a partir de la suma de los pesos multiplicados por los valores de entrada correspondientes
  - Afectan directamente la capabilidad y el rendimiento de la red neuronal 
- `Activation for Hidden Layers`
  - Una red neuronal puede tener cero o más capas ocultas
  - Se pueden tener funciones de activación más complejas, que pueden ayudar al rendimiento de la red neuronal
- `ReLU` ***(Rectified Linear Activation Function)***
  - Si la entrada es negativa, retorna 0
  - Si es positiva o 0, retorna la misma entrada
- `Sigmoid Hidden Layer Activation Function`
  - Usada en el algoritmo de regresión logística
  - Mientras mayor el valor, más cercano a 1
  - Mientras menor el valor, más cercano a -1
  - La función está dada por $\frac{1}{1+e^{-x}}$.
- `Tanh Hidden Layer Activation Function`
  - Muy similar a la sigmoide
  - Mientras mayor el valor, más cercano a 1
  - Mientras menor el valor, más cercano a -1
  - La función está dada por $\frac{e^x - e^{-x}}{e^x+e^{-x}}$.
- `How to Choose a Hidden Layer Activation Function`
  - Depende de la arquitectura de la red neuronal:
    - **`Multilayer Perceptron (MLP):`** ReLU activation function.
    - **`Convolutional Neural Network (CNN):`** ReLU activation function.
    - **`Recurrent Neural Network:`** Tanh and/or Sigmoid activation function
- `Activation for Output Layers`
  - Tres tipos principales:
    - **`Linear Output Activation Function:`** ninguna activación (retornar el valor de entrada)
    - **`Sigmoid Output Activation Function:`** aplicar la función sigmoide para la capa de salida
    - **`Softmax OUtpout Activation Function:`** sumar todos los valores de salida usando $\frac{e^x}{\sum e^x}$
- `How to Choose a Hidden Layer Activation Function`
  - Depende del objetivo de la red neuronal y el problema en cuestión:
    - Clasificación:
      - **`Binary Classification:`** One node, sigmoid activation.
      - **`Multiclass Classification:`** One node per class, softmax activation.
      - **`Multilabel Classification:`** One node per class, sigmoid activation.
    - Regresión: **`Linear Activation`**

### Comentarios

Me parece que este tutorial responde bastante bien una de las dudas que tenía para las redes neuronales, ya que nunca se había abarcado en el curso de `Inteligencia Artificial` las diferencias entre estas funciones de activación.

### Dudas

No tengo ninguna duda, ya que el tutorial fue bastante claro y conciso explicando las funciones de activación.