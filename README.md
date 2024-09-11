# Deteccion-y-Clasificacion-de-Micorrizas
## Autores:

1. David Paredes
2. Jordy Loor
3. Abraham Jimenez
4. Diego Ortiz
   
## Contexto:
El proyecto consiste en la creación de un modelo que pueda detectar y clasificar dos tipos de micorrizas: 
  * Endomicorrizas y Ectomicorrizas.
    
## Repositorio de las imágenes:
https://github.com/jalm0911/Micorrizas

## Funciones:
Se realiza primero la creación del dataset de imágenes de las micorrizas (1000 imágenes como mínimo), con un tamaño de (150x150)pixeles para asegurar uniformidad.
Posteriormente de haber importado librerías y definir rutas se procede a cargar las imágenes de Ectomicorrizas y Endomicorrizas.

## División del Conjunto de Datos:
En esta sección del código se cargan imágenes de micorrizas desde 2 directorios diferentes, se extraen características relevantes de las imágenes que serán utilizadas como entrada para el modelo.
Cada fila corresponde a un conjunto de características de una imagen, para el caso de nuestro proyecto, estas características son:
* Color y Forma.

## Búsqueda de los mejores parámetros: 
  * Param_grid:

    Define las combinaciones de hiperparámetros que el modelo SVM va a probar.

    
  * Grid_search:
    
     Método de busqueda que toma en cuenta diferentes combinaciones de hiperparámetros y elige la combinación que arroja un margen de error más bajo.

## Entrenamiento del modelo con los mejores parámetros: 
* Creación del modelo:

    Se crea un modelo SVM con parámetros optimizados (best_params) y se configuran para que devuelva probabilidades de clasificación.

* Entrenamiento del modelo:
  
    Se entrena el modelo con datos de entrenamiento (X_train y y_train). Esto permite que el modelo aprenda a clasificar los datos en función de las características y etiquetas.
  
## Conclusión:
El modelo SVC entrenado para la clasificación de micorrizas demostró un alto rendimiento, alcanzando una exactitud de 97.13%. Esto sugiera que es capaz de distinguir eficazmente entre ectomicorrizas y endomicorrizas con una precisión y recall elevados para ambas clases.

El análisis de la matriz de confusión revela un bajo número de errores, principalmente en la clasificación de endomicorrizas. El modelo también muestra una gran capacidad para predecir nuevas imágenes con una alta certeza, como se observa en la predicción de una endomicorriza con una probabilidad del 99.35%.
  
