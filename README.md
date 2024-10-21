Implementacion:

Correr el script the PreProcesamiento para generar los archivos pickle necesarios.
Entrenar un Modelo Como el OrdinalPolicyNetwork o BasicTransformers.
El entrenamiento genera un archivo de modelo con los mejores resultados obtenidos.
Correr el script de inferencia para generar predicciones y submission files.

Se agregan dos implementaciones del modelo. Una basica de Transformers y un modelo tipo policy network. Para la competencia el modelo sencillo funciono mejor con corridas de hasta 54k en kaggle. El modelo de PolicyNetwork tiene la ventaja de proder predicir hasta BAJA+3 y BAJA+4 pero dio una ganacia no superior a 35K.

Ambos modelos sufren de "future peeking", le prestan atencion a toda la serie temporal para predecir un estado. Un modelo de regresion o con una mascara causal podrian mejorar la performance.

TODO:Modelo de regresion

Ambos modelos pueden ser entrenados con el flag Optuna para la optimizacion de hyperparametros.
El script OptunaRead nos permite leer las corridas de Optuna.
