# Predicción de Cancelación de Clientes (Churn) — Telecom X

##  Descripción
Este proyecto corresponde al **Desafío Telecom X**, cuyo objetivo es **predecir la cancelación de clientes** (*churn*) en una empresa de telecomunicaciones.  
A partir de un dataset tratado y balanceado, se entrenaron y evaluaron distintos modelos de Machine Learning, identificando además los factores que más influyen en la decisión de cancelar.

---

##  Estructura del proyecto
- `telecomx_limpio.csv` → archivo de datos limpio y estandarizado.  
- `notebook.ipynb` → cuaderno principal con el flujo de análisis, modelado y evaluación.  
- `informe_churn.md` → informe en formato Markdown con resultados y recomendaciones.  
- `README.md` → este archivo de documentación.  

---

##  Metodología
1. **Preprocesamiento**
   - Eliminación de columnas irrelevantes (ID y duplicados).
   - Codificación de variables categóricas (One-Hot Encoding).
   - Balanceo de clases en *train* con **SMOTE**.
   - Escalado de variables para modelos sensibles a la escala.

2. **Modelado**
   - **Regresión Logística** (requiere normalización).  
   - **Random Forest** (no requiere normalización).  

3. **Evaluación**
   - Accuracy, Precisión, Recall, F1-score, ROC-AUC.  
   - Matrices de confusión y curvas ROC.  

---

##  Resultados principales

| Modelo               | Accuracy | Precisión | Recall | F1-score | ROC-AUC |
|----------------------|----------|-----------|--------|----------|---------|
| **Regresión Logística** | **0.771** | **0.562** | **0.634** | **0.595** | **0.825** |
| Random Forest        | 0.764    | 0.553     | 0.586  | 0.569    | 0.813   |

 **Conclusión:**  
- La **Regresión Logística** tuvo mejor desempeño general y es recomendada como línea base.  
- Los factores más influyentes en la cancelación son:
  - **Alta facturación mensual/total.**
  - **Baja antigüedad.**
  - **Contrato mensual.**
  - **Ausencia de servicios adicionales (seguridad, soporte, TV, películas).**

---

##  Recomendaciones de negocio
- Diseñar **estrategias de retención** para clientes nuevos con facturación alta.  
- Incentivar la **migración de contratos mensuales a anuales**.  
- Incluir **servicios complementarios** (soporte, seguridad, TV/películas) en paquetes de valor.  
- Implementar **programas de onboarding** y soporte prioritario en los primeros 90 días.  

---

##  Tecnologías utilizadas
- **Python 3.10**  
- Librerías: `pandas`, `numpy`, `scikit-learn`, `imblearn`, `matplotlib`, `seaborn`  

---

##  Autor
Proyecto desarrollado como parte del **Desafío de Machine Learning — Telecom X**.  
Elaborado por Yulitza Gamez.
