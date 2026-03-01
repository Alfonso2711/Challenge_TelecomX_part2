<div align="center">
  
  # 📞 Predicción de Fuga de Clientes (Churn) - TelecomX
  
  **Proyecto de Machine Learning para la retención estratégica de usuarios en el sector de Telecomunicaciones.**
  
  [![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](#)
  [![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](#)
  [![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](#)
  [![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](#)

</div>

---

## 🎯 Misión del Proyecto

> Desarrollar modelos predictivos capaces de identificar qué clientes tienen mayor probabilidad de cancelar sus servicios, permitiendo a la empresa anticiparse al problema y tomar decisiones de retención basadas en datos.

## 🛠️ Flujo de Trabajo (Pipeline)

1. **Preparación de Datos:** Limpieza, manejo de nulos, y *One-Hot Encoding* para variables categóricas.
2. **Estandarización y Balanceo:** Uso de `StandardScaler` y técnicas de *Oversampling* para lidiar con el desbalanceo de clases (Churn: 25% vs Retención: 75%).
3. **Análisis Exploratorio (EDA):** Identificación de variables críticas mediante matrices de correlación y visualización bivariada.
4. **Modelado Predictivo:** Entrenamiento y comparación de algoritmos de clasificación.

---

## 🤖 Evaluación de Modelos

Se entrenaron dos modelos principales bajo el mismo conjunto de datos (80% entrenamiento / 20% prueba) para contrastar su desempeño:

| Modelo | Tratamiento de Datos | Exactitud (Accuracy) | Recall (Churn=1) | Diagnóstico | Veredicto |
| :--- | :---: | :---: | :---: | :--- | :--- |
| **Regresión Logística** | Normalizados | 75.38% | **82.26%** | Excelente generalización | 🏆 **Modelo Ganador** |
| **Random Forest** | Sin Normalizar | **79.57%** | 59.41% | *Overfitting* (99% en Train) | Descartado |

**¿Por qué ganó la Regresión Logística?** En un problema de retención, el peor error es dejar ir a un cliente por no detectarlo (*Falso Negativo*). Aunque el Random Forest tuvo mejor exactitud general, la Regresión Logística logró detectar al **82% de los clientes reales que iban a cancelar**, dándole a la empresa un margen de acción altísimo.

---

## 💡 Insights Estratégicos (Hallazgos Clave)

Tras analizar la importancia de las variables (coeficientes de la regresión y reducción de impureza del árbol), el perfil de mayor riesgo es claro:

* 🚨 **El Peligro del "Mes a Mes":** Los clientes sin contratos a largo plazo representan casi la totalidad de las bajas. **Recomendación:** Ofrecer incentivos para migrar a contratos de 1 o 2 años.
* 🚨 **Alerta en Fibra Óptica:** Es el servicio con la correlación positiva más alta hacia el abandono. **Recomendación:** Realizar una auditoría técnica urgente o revisar la oferta de los competidores locales.
* 🟢 **Lealtad Financiera:** El mayor riesgo de fuga ocurre en los primeros 12 meses. Una vez cruzada esa barrera, el usuario se vuelve altamente leal, sin importar tanto el costo mensual.

---

## 🚀 Cómo ejecutar este proyecto localmente

1. Clona este repositorio en tu máquina:
   ```bash
   git clone [https://github.com/Alfonso2711/Challenge_TelecomX_part2.git](https://github.com/Alfonso2711/Challenge_TelecomX_part2.git)
