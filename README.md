Para correr el modelo primero correr el script prepro the prepocesamiento para generar los archivos pickle necesarios.
Se recomiendo hacerlo en dos partes primero hasta el checkpoint 1 y luego desde el checkpoint 2 para utlizar menos emoria ram. Con 64gb de ram y 64gb de swap funciona.

Una vez generados los archivos pickle se puede correr el OrdinalPolicyNetwork para entrenar un modelo o correrlo con el flag de Optuna para optimizar los hyperparametros.

El script OptunaRead permite leer la bd creada por optuna

PolicyPredictor permite usar un modelo para la inferencia y crear la submission para la competencia.
Para el entrenamiento del modelo se sacaron los ultimos dos ultimos meses en el prepropecesamiento, generar otro pickle con los 33 meses necesarios para la compentencia.

El script de inferencia automaticamente usa el ultimo mes para la submission.

Para este modelo se agregaron las clases BAJA+3 BAJA+4.

TODO: Hacer mas prolijo el codigo
