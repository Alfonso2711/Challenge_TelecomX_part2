📞 Predicción de Churn - TelecomX (Challenge Parte 2)
Este proyecto de Data Science tiene como objetivo desarrollar modelos predictivos de Machine Learning capaces de identificar qué clientes de una empresa de telecomunicaciones tienen mayor probabilidad de cancelar sus servicios (Churn).

Al anticiparnos a la cancelación, la empresa puede tomar decisiones estratégicas de retención para reducir pérdidas.

🎯 Objetivos del Proyecto
Preparación de datos: Limpieza, codificación (One-Hot Encoding), estandarización y balanceo de clases.

Análisis Exploratorio (EDA): Identificación de variables críticas mediante matrices de correlación y visualización bivariada.

Modelado Predictivo: Entrenamiento y comparación de modelos de clasificación.

Conclusiones Estratégicas: Extracción de insights de negocio basados en la importancia de las variables.

🛠️ Herramientas y Tecnologías
Lenguaje: Python

Manipulación de Datos: Pandas, NumPy

Machine Learning: Scikit-Learn (Regresión Logística, Random Forest, StandardScaler)

Visualización: Matplotlib, Seaborn

🤖 Modelos Evaluados
Se entrenaron dos modelos principales para comparar su rendimiento frente a la detección de cancelaciones:

Regresión Logística (Modelo Ganador): Se entrenó con datos normalizados. Aunque su exactitud global fue del 75%, logró un Recall del 82%, haciéndolo el modelo ideal para el negocio ya que prioriza detectar a la mayor cantidad posible de clientes en riesgo de fuga para intervenirlos a tiempo.

Random Forest: Se entrenó sin normalizar. Presentó sobreajuste (overfitting), logrando un 99% de exactitud en entrenamiento pero cayendo al 79% en prueba, con un Recall bajo (59%).

📊 Principales Hallazgos (Insights de Negocio)
El análisis de la importancia de variables y correlaciones reveló el siguiente perfil de riesgo:

El peligro del "Mes a Mes": Los clientes sin contrato a largo plazo son casi la totalidad de las bajas. Ofrecer contratos a 1 o 2 años es la estrategia de retención número uno.

El problema de la Fibra Óptica: Es el servicio con la correlación positiva más alta hacia el abandono. Requiere una auditoría urgente de calidad de red o precios frente a la competencia.

Lealtad financiera: Los primeros 12 meses son críticos. Superada esa barrera de tiempo, la probabilidad de cancelación se desploma drásticamente.
