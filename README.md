# Sistema de Detección de Fraude con Machine Learning

Proyecto de **Machine Learning** para detectar transacciones fraudulentas utilizando datos históricos.  
Incluye **preprocesamiento**, manejo de **clases desbalanceadas**, entrenamiento de modelos (baseline → modelos avanzados), evaluación con métricas adecuadas (Precision/Recall/F1/PR-AUC) y **explicabilidad**.

---

## Objetivo

Construir un modelo capaz de **identificar transacciones fraudulentas** minimizando:
- **Falsos negativos** (fraudes no detectados) → alto impacto financiero
- **Falsos positivos** (bloqueos innecesarios) → mala experiencia del cliente

---

##  Enfoque y metodología

1. **EDA** (Exploración de datos): distribución, outliers, correlaciones y fugas de información (leakage).
2. **Preprocesamiento**: limpieza, encoding, escalado y manejo de nulos.
3. **Desbalance de clases**:
   - `class_weight='balanced'` (cuando aplica)
   - Oversampling (ej. SMOTE) y/o undersampling (según experimento)
4. **Modelado**:
   - Baseline: Logistic Regression
   - Avanzados: Random Forest / XGBoost / LightGBM (según disponibilidad)
5. **Evaluación**:
   - Matriz de confusión
   - **Precision, Recall, F1**
   - **PR-AUC** (prioritaria en fraude)
   - ROC-AUC (referencial)
6. **Interpretabilidad**:
   - Feature importance
   - SHAP (si aplica)
7. **Predicción**:
   - Score de riesgo y umbral configurable (threshold tuning)

---

##  Métricas (por qué no basta Accuracy)

En fraude, la clase positiva (fraude) suele ser muy pequeña.  
Por eso se prioriza:
- **Recall**: capturar la mayor cantidad de fraudes
- **Precision**: reducir alertas falsas
- **F1**: balance entre ambas
- **PR-AUC**: más informativa que ROC-AUC con clases desbalanceadas

---

##  Tecnologías

- Python
- Pandas / NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE, etc.)
- XGBoost / LightGBM (opcional)
- Matplotlib / Seaborn
- SHAP (opcional)

---

## 📁 Estructura del repositorio

