Entropía y arboles de decisión

Ordenamos las variables desde las más informativas para que el arbol vaya en ese orden.
Esta es la forma mas eficiente de hacer el arbol.  

Se calculan las _information gain_ de todas las variables y las que más hagan reducir la entropía son las más informativas y son por las que voy a comenzar.  

Tengo que limitar la profundidad del árbol para evitar el overfit (lo defino yo manualmente).  
Random forest (bosques de decición, conjunto de árboles de decisión) es una forma de evitar el overfit (sobre-ajuste) en arboles de decisión.  
**XGBoost** es de los más usados hoy. En sklearn hay varias implementaciones para trabajar con árboles.  

Puedo definir cual es el territorio donde mis predicciones son válidas y cuando llegue un valor nuevo fuera de ese territorio **responder que no hay predicción**.  

El error sobre el dataset de entrenamiento baja a medida que ajusto hasta llegar a cero.  
Si veo esa misma curva de cantidad de errores sobre los datos de text o validación el error va a bajar hasta un punto de pico minimo y luego comienza a subir. Ese es el overfit.  

Si tengo pocos datos puedo hacer este proceso usando muestras y test diferentes y calcular el promedio y desvio de los _accuracies_

_Internal cross validation_: el conjunto de entrenamiento (despues de sacar la de test) se separa en n partes. Se hacen múltiples separaciones y cada una de ellas es el conjunto de _validación_ de una iteracion. Con todas estas iteraciones veo la estabilidad y variabilidad de los errores (medidos en gráficos para detectar el overfit por ejemplo). Generalmente usamos 5 o 10 paquetes. Mientras más conjuntos hay estos se vuelven más chiquitos y mientras más tambien es más robusto el resultado que me da.  

[Acá](https://github.com/DiploDatos/IntroduccionAprendizajeAutomatico/blob/master/archive/2018/Clase%204%20-%20Metricas%20y%20validacion%20de%20resultados.ipynb) veo ejemplos de matriz de confusión (muestra como clasifico cada clase y los errores).  

Las matrices de confusión me da detalles de como fallan las clasificaciones mas allá de un numero simple como puede ser el _accuracy_. Quizás anda pésimo en algunas clases y no lo veo solo en un número.  

Las _curvas ROC_ me ayudan con predicciones binarias. Se usa también las curvas _precision_ + _recall_.  







