# 📉 Challenge-Telecom_X-Parte2
## :dart: Objetivo: 
#### La empresa Telecom X quiere anticiparse al problema de cancelación por lo que se pretende desarrollar modelos predictivos capaces de prever a los clientes que tienen mayor probabilidad de cancelar los servicios. 
🧠 Objetivos del Desafío

✔️Preparar los datos para el modelado (tratamiento, codificación, normalización).

✔️Realizar análisis de correlación y selección de variables.

✔️Entrenar dos o más modelos de clasificación.

✔️Evaluar el rendimiento de los modelos con métricas.

✔️Interpretar los resultados, incluyendo la importancia de las variables.

✔️Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.


## 🛠️Tecnologías utilizadas
![Static Badge](https://img.shields.io/badge/Python-blue?style=for-the-badge&logo=python&logoColor=yellow&logoSize=auto&labelColor=gray&color=blue&cacheSeconds=3600)
![Static Badge](https://img.shields.io/badge/Pandas-blue?style=for-the-badge&logo=pandas&logoColor=white&logoSize=auto&labelColor=gray&color=blue&cacheSeconds=3600)
![Static Badge](https://img.shields.io/badge/Numpy-navy?style=for-the-badge&logo=numpy&logoColor=white&logoSize=auto&labelColor=navy&color=navy&cacheSeconds=3600)
![Static Badge](https://img.shields.io/badge/Matplotlib-white?style=for-the-badge&logo=matplotlib&logoColor=white&logoSize=auto&labelColor=black&color=white&cacheSeconds=3600)

![Static Badge](https://img.shields.io/badge/seaborn-purple?style=for-the-badge&logo=seaborn&logoColor=white&logoSize=auto&labelColor=white&color=purple&cacheSeconds=3600)
![Static Badge](https://img.shields.io/badge/colab-gray?style=for-the-badge&logo=googlecolab&logoColor=orange&logoSize=auto&label=google&labelColor=gray&color=gray&cacheSeconds=3600)

## 💻 Preparación de datos:
#### 🔸Extracción de datos
#### 🔸Pre procesamiento
#### 🔸Análisis dirigido: cómo variables específicas como gasto total o tiempo de contrato se relacionan con la cancelación
<img width="790" height="590" alt="image" src="https://github.com/user-attachments/assets/0f11bab2-801b-42b4-9245-7cf1b0add8b7" />
<img width="790" height="590" alt="image" src="https://github.com/user-attachments/assets/f03170ef-4ca7-424c-94bb-4ea81f2789d1" />

## 📊 EDA
## Correlación entre variables númericas y categóricas 
🟡Antigüedad_Meses (Tenure): Correlación negativa másfuerte con la deserción (-0.35).

👉Esto sugiere que los clientes con más antigüedad son menos propensos a abandonar el servicio.

🟡Cargo_Mensual: correlación negativa debil con la deserción (alrededor de 0.19).

👉Esto indica que un cargo mensual o un cargo diario más alto se asocian con una menor probabilidad de deserción.

🟡Cuentas_Diarias y mensuales: correlación positiva debil (alrededor de 0.19).

👉Clientes con cargos mensuales más altos tienen ligeramente mayor probabilidad de cancelar.

🟡Seguridad_Online y Soporte_Tecnico: correlaciones negativas moderadas con la deserción (alrededor de -0.17 y -0.16 respectivamente).

👉Los clientes que tienen estos servicios son menos propensos a irse.

## 🔍Análisis Comparativo de Modelos

| Modelo | F1-Score | Recall | Accuracy | Comentarios |
| :--- | :--- | :--- | :--- | :--- |
| Regresión Logistica | 0.87/0.58 | 0.90/0.52 | 0.80 | ⚠️El modelo de Regresión Logística tiende a favorecer a la clase mayoritaria (no deserción). |
| Random Forest | 0.86/0.53  | 0.90/0.47 | 0.78 | ⚠️El modelo solo pudo identificar correctamente el 47% de todos los clientes que realmente desertaron. |
| Regresión logística balanceada |0.81/0.63 | 0.73/0.79 | 0.75 | ✅El Modelo de Regresión Logística Balanceada es el mejor entre estos dos. Logra un Recall más alto para la clase de deserción (79% vs 71%) y tiene un número significativamente menor de Falsos Negativos (79 vs 109).
| Regresión Logística con balanceo y SMOTE |0.81/0.60 |  0.76/0.71 |  0.74 | ⚠️Cuando el modelo predice que un cliente sí desertará, es correcto el 51% de las veces. Esta precisión es la más baja de los modelos probados

## ⭐Modelo de Regresión Logística Balanceada - Champion⭐
### ⭐Mejor Detección de Desertores (Recall y Falsos Negativos): Logró el Recall más alto para la clase de deserción (aproximadamente un 79%), lo que significa que detectó a casi el 80% de los clientes que realmente se fueron.

Esto se traduce en el menor número de Falsos Negativos (clientes que desertaron pero el modelo no pudo predecir), lo cual es crucial, ya que perder un cliente es a menudo más costoso que una intervención innecesaria.

⭐Equilibrio de Costos: Aunque puede tener un costo ligeramente mayor en Falsos Positivos (predicciones de deserción incorrectas), es aceptable porque el beneficio de salvar a un cliente real supera el costo de contactar a uno que no iba a desertar.

⭐Superioridad sobre otros modelos: Superó a la Regresión Logística normal y a Random Forest en su capacidad para identificar desertores, y tuvo un rendimiento marginalmente mejor (o al menos más favorable en cuanto a Falsos Negativos) que la Regresión Logística con SMOTE.


<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/56af56cf-8b54-48dc-bf74-577edc161bc9" />

## 🔐Modo de ejecución:
✔️Clonar el repositorio

✔️Abre el archivo 

✔️Carga el archivo [datos_tratados_Telecom_parte2](datos_tratados_Telecom_parte2)

✔️Ejecuta las celdas
