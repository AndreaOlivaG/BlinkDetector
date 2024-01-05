# BlinkDetector
## Objetivo del proyecto
En este proyecto se abordan dos aproximaciones para la tarea de predicción de parpadeo a través de pares de imágenes de ojos. Dado que se trata de imágenes, los modelos entrenados deben ser redes neuronales convolucionales.

La primera aproximación consiste en construir y entrenar una red neuronal convolucional desde cero y entrenar la totalidad de sus parámetros. Esta red cuen- ta con una capa de entrada, varias capas convolucionales y de pooling, una flatten, y dos fully-connected, siendo la última de ellas la capa de salida, la cual posee una única unidad neuronal, dado que se trata de un problema de clasificación binaria.

Por otro lado, la segunda aproximación consiste en utilizar una red convolu- cional ya entrenada y modificarla, adaptándola a este problema, lo que se conoce como transfer learning. Se ha elegido que el modelo utilizado sea DenseNet121 entrenado sobre ImageNet, que destaca entre el resto de redes pre-entrenadas por ser la que menor número de parámetros tiene y menor tamaño ocupa.

Asimismo, en ambas aproximaciones, la función de pérdidas es BinaryFocal- Crossentropy, la cual obtiene buenos resultados cuando el dataset está desbalan- ceado, puesto que la penalización es menor cuando las instancias son más fáciles de predecir, y mayor cuando son más difíciles, que es el caso de los ojos cerrados.

En cuanto al algoritmo de optimización, se utiliza Adam.
