#programming #ai

### ¿Qué es un Perceptrón?

Un Perceptrón es una unidad de procesamiento que toma un vector de entradas, las multiplica por un vector de pesos, las suma y luego aplica una [función de activación](obsidian://open?vault=Obsidian%20Vault&file=Programming%2FAI%2FFunciones%20de%20activacion.canvas) para determinar la salida. En su forma más simple, la función de activación es una función escalón que devuelve 1 si la suma ponderada es mayor que un umbral y -1 en caso contrario.
## Perceptron multicapa

El **perceptrón multicapa** es una [red neuronal artificial](https://es.wikipedia.org/wiki/Red_neuronal_artificial "Red neuronal artificial") (RNA) formada por múltiples capas, de tal manera que tiene capacidad para resolver problemas que no son linealmente separables, lo cual es la principal limitación del [perceptrón](https://es.wikipedia.org/wiki/Perceptr%C3%B3n "Perceptrón") (también llamado perceptrón simple). El perceptrón multicapa puede estar totalmente o localmente conectado. En el primer caso cada salida de una neurona de la capa "i" es entrada de todas las neuronas de la capa "i+1", mientras que en el segundo cada neurona de la capa "i" es entrada de una serie de neuronas (región) de la capa "i+1".

![[Pasted image 20250209123840.png]]

### Tipos de capas

Las capas pueden clasificarse en tres tipos:

- Capa de entrada: Constituida por aquellas neuronas que introducen los patrones de entrada en la red (Los vectores con las características que se usaran para el análisis). En estas neuronas no se produce procesamiento.
- Capas ocultas: Formada por aquellas neuronas cuyas entradas provienen de capas anteriores y cuyas salidas pasan a neuronas de capas posteriores.
- Capa de salida: Neuronas cuyos valores de salida se corresponden con las salidas de toda la red.

La [propagación hacia atrás](https://es.wikipedia.org/wiki/Propagaci%C3%B3n_hacia_atr%C3%A1s "Propagación hacia atrás") (también conocido como retropropagación del error o [regla delta](https://es.wikipedia.org/w/index.php?title=Regla_delta&action=edit&redlink=1 "Regla delta (aún no redactado)") generalizada), es un algoritmo utilizado en el entrenamiento de estas redes, por ello, el perceptrón multicapa también es conocido como red de retropropagación (no confundir con la red de contrapropagación).

## Sklearn Perceptron

La clase `Perceptron` en `scikit-learn` tiene varios parámetros que pueden ser ajustados para controlar el comportamiento del modelo. Aquí están los más importantes:

1. **`penalty`**:
    
    - **Descripción**: La norma utilizada en la penalización (`'l2'`, `'l1'`, `'elasticnet'` o `None`).
    - **Valor por defecto**: `None`.
2. **`alpha`**:
    
    - **Descripción**: Parámetro de regularización (debe ser un valor positivo).
    - **Valor por defecto**: `0.0001`.
3. **`fit_intercept`**:
    
    - **Descripción**: Si se debe ajustar el intercepto (sesgo) del modelo.
    - **Valor por defecto**: `True`.
4. **`max_iter`**:
    
    - **Descripción**: Número máximo de iteraciones (pasadas por los datos) para el algoritmo de entrenamiento.
    - **Valor por defecto**: `1000`.
5. **`tol`**:
    
    - **Descripción**: Criterio de tolerancia para la convergencia. Si la pérdida no disminuye en al menos `tol` después de una iteración, el algoritmo se detiene.
    - **Valor por defecto**: `1e-3`.
6. **`shuffle`**:
    
    - **Descripción**: Si se deben mezclar las muestras cada vez que se pasa por los datos.
    - **Valor por defecto**: `True`.
7. **`eta0`**:
    
    - **Descripción**: Tasa de aprendizaje inicial.
    - **Valor por defecto**: `1.0`.
8. **`n_jobs`**:
    
    - **Descripción**: Número de CPU a utilizar para el cálculo. `-1` significa usar todos los procesadores disponibles.
    - **Valor por defecto**: `None`.
9. **`random_state`**:
    
    - **Descripción**: Semilla utilizada por el generador de números aleatorios para asegurar la reproducibilidad.
    - **Valor por defecto**: `None`.
10. **`early_stopping`**:
    
    - **Descripción**: Si se debe usar parada temprana para terminar el entrenamiento cuando la pérdida no mejora.
    - **Valor por defecto**: `False`.
11. **`validation_fraction`**:
    
    - **Descripción**: Proporción del conjunto de entrenamiento que se utilizará como conjunto de validación si se utiliza parada temprana.
    - **Valor por defecto**: `0.1`.
12. **`n_iter_no_change`**:
    
    - **Descripción**: Número de iteraciones sin cambio en la pérdida para detener el entrenamiento cuando se utiliza parada temprana.
    - **Valor por defecto**: `5`.
13. **`class_weight`**:
    
    - **Descripción**: Peso asociado a cada clase. Si no se especifica, todas las clases tienen el mismo peso.
    - **Valor por defecto**: `None`.
14. **`warm_start`**:
    
    - **Descripción**: Si se debe reutilizar la solución de la llamada anterior para ajustar el modelo y agregar más iteraciones.
    - **Valor por defecto**: `False`.