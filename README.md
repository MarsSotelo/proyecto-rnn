# proyecto-rnn
 Proyecto de Redes Neuronales Recurrentes (RNN)

**Entrega: 11 de abril**  
**Autor: Mario Alberto Tapia Sotelo**

Este proyecto aplica modelos de redes neuronales recurrentes, específicamente LSTM, para predecir la temperatura mensual en Ciudad de México usando datos históricos, es una implementación práctica de los conceptos vistos en clase sobre aprendizaje secuencial con Deep Learning...

---------------------------------------------------------------------------------------------------

## Breve Descripción

Se trabajó con el archivo `GlobalLandTemperaturesByCity.csv`, descargado en "KAGGLE" el cual contiene registros históricos de temperatura por ciudad a nivel mundial...
Para simplificar el análisis y enfocarlo, se hizo una copia de la base de datos y tome solo la ciudad de Mexico que es de mi interes y al final cortamos la base de datos original para formar asi un subconjunto con datos **exclusivamente de Ciudad de México**, guardado como `df_ciudad_mexico.csv` solo para poder subirlo aqui y asi cualquier persona pueda replicar este proyecto sin usar toda la base de datos asi como lo hice yo...

-----------------------------------------------------------------

##  Objetivo Principal

Aplicar modelos de redes neuronales recurrentes (RNN), comprendiendo su estructura, funcionamiento interno y utilidad para predecir series temporales

-----------------------------------------------------------------------------------------------

## Enfoque y Justificación

- Se utilizó una arquitectura **LSTM (Long Short-Term Memory)**, que pertenece a la familia de las RNN, capaz de capturar dependencias de largo plazo en secuencias de datos...
- Se justificó el uso de LSTM por su capacidad de **manejar series temporales no lineales y con memoria**, como lo es una serie climática mensual...
- Se probaron distintas configuraciones con:
  - Capas apiladas (stacked)
  - Regularización con Dropout
  - Diferentes optimizadores: **Adam** y **RMSprop**

---------------------------------------------------

## Dataset

Archivo: `df_ciudad_mexico.csv` by `GlobalLandTemperaturesByCity.csv`
Columnas principales:
- `dt`: Fecha
- `AverageTemperature`: Temperatura promedio mensual
- `Temp_norm`: Versión normalizada usada para entrenamiento

--------------------------------------

## Ahora el Modelo y Librerías

- `tensorflow.keras.models.Sequential`
- Capas: `LSTM`, `Dense`, `Dropout`
- Optimización con `Adam` y `RMSprop`
- Pérdida: `mean squared error (mse)`
- Gráficas con `matplotlib`

--------------------------------------------------
## Consejo
Si usas visual studio code necesitas tener Python 10.0 que causa menos problemas con tensorflow

------------------------------------------------------------------------

## Requisitos

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow...


