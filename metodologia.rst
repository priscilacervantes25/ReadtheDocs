.. raw:: html

    <h1 style="color:#1565C0;">Metodología</h1>


.. raw:: html

    <h1 style="color:royalblue;">SARIMAX</h2>

EXPLICACIÓN

.. raw:: html

    <h1 style="color:royalblue;">FFNN</h2>    

- Selección de hiperparámetros:

    Se tuvo que considerar el número de lags, en este caso se usaron los últimos 7 días como entradas, para que aprendiera dependencias más recientes.

    Para las capas, está compuesta por tres ocultas densas con 64, 32 y 8 neuronas.

    Por otro lado, en la función de activación, se empleó la función **ReLU** en las capas ocultas, y una función lineal en la capa de salida para predecir valores continuos.

    Se aplicó `Adam` como optimizador y para la regularización se usó `EarlyStopping` (patience=15) para evitar el sobreajuste.

- Esquema de Walk-Forward y validación

    Este paso es primordial ya que se evalúa el desempeño del modelo y para entrenar conforme la serie temporal avanza(se actualiza) para lograr hacer pronósticos lo mejor posible. 

    Los pasos que se realizaron fueron la división del conjunto de datos en entrenamiento, validación y prueba. El modelo entrenado bajo este esquema generó los pronósticos para los siguientes 5 días hábiles (20–24 de octubre de 2025).
