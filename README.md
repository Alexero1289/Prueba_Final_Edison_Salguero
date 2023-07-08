# Prueba_Final_Edison_Salguero
## MODELO NEURONAL PARA PREDICCIÓN DE TIPOS DE CARNES
En el presente modelo se utiliza TENSORFLOW, que es una biblioteca de código abierto desarrollada por Google y permite construir modelos de aprendizaje automático, especialmente redes neuronales.
Adicional se utiliza 'tf.keras' es una API de alto nivel para la construcción y entrenamiento de modelos de aprendizaje profundo en TensorFlow. Proporciona una interfaz conveniente y fácil de usar para desarrollar redes neuronales y otros modelos de aprendizaje profundo.
## LIBRERIAS
Se colocan todas las librerias y variables que se utilizan en el proyecto
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/971d05f9-6d5c-4d7f-82ea-f05ebe7b721f)
## EXTRACCIÓN DE IMAGENES Y CREACIÓN DE DATA SET PARA ENTRENAMIENTO DEL MODELO
Se utiliza la función 'tf.keras.utils.image_dataset_from_directory' de TENSORFLOW que permite cargar imágenes desde los directorios donde se tienen las imagenes de entrenamiento y crea dos dataset de imágenes, 1 data set de entrenamiento y 1 data set de validación conformado con el 20% de toda la data; estos para posterior uso en tareas de aprendizaje automático.
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/18be7e3f-371c-4dec-bbc1-3fe9dcabe5a7)
## CONFIGURACIÓN DEL MODELO
Mediante la clase 'tf.keras.Sequential' de TensorFlow se construye y configura el modelo de aprendizaje profundo; considerando que en este tipo de modelo, las salidas de una capa se alimentan directamente a la siguiente capa. En este caso se utilizan 5 capas con diferentes números de neuronas y al final se crea la capa de salida con 8 neuoronas que representan a las 8 clases que se tienen en la data.
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/59257f12-a5c4-451f-818b-5e0471142bc9)
## COMPILACIÓN DEL MODELO
Se procede a la compilación del modelo, utilizando el algoritmo de optimización 'adam', función de pérdida 'loss' para evidenciar que tan bien se está desempeñando el modelo en términos de la diferencia entre las predicciones y las etiquetas verdaderas; y, metrica  'accuracy' para calcular la precisión del modelo.
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/cf043137-2a0b-4355-a422-642accddb44b)
## ENTRENAMIENTO DEL MODELO
Mediante el método '.fit()' se procede a entrenar el modelo, indicando lote de datos de 64 con 20 epocas.
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/ec8270e8-05d7-4d11-879f-651e5504d938)
## EVALUACIÓN DEL MODELO
Se extrae los datos de entrenamiento y pruebas para porteriormente pasar los datos por el modelo creado, obteniendo resultados sobre el 98% y 85% de acierto, siendo estos valores aceptables para el tipo de data que se dispone. El modelo podria mejorar su predicción aumentando el número de epocas al momento del entrenamiento. A continuación se presentan los resultados a traves de la matrzi de confusión. 
### Evaluación del modelo con la imagenes de entrenamiento
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/e345dad0-3de3-4ff4-adbe-4a574b43619a)
### Evaluación del modelo con la imagenes de pruebas
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/55172d76-b000-4f6a-8826-d79fdaf3d8d4)
## PRUEBA EXTRA
Se elige un dato 300 de data set de pruebas para pasarlo por el modelo, cuyo resultado es clase 7 con un 99.98% de exactitud ;y, se contrasta el resultado con el grafico del dato, evidenciando que la predicción es correcta y su nivel de exactitud es muy bueno.
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/0b3f4b5a-0c68-4808-a832-88dd82470cbe)
### Resultado con alto nivel de exactitud
![image](https://github.com/Alexero1289/Prueba_Final_Edison_Salguero/assets/136047935/dd7515ff-db86-4144-86f8-934047710886)
