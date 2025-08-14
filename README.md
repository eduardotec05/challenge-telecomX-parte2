# 📊 Predicción de Churn en Clientes de Telecomunicaciones

## 📌 Descripción del Proyecto  
Este proyecto implementa un **pipeline completo de análisis y modelado predictivo** para identificar clientes con alta probabilidad de cancelar el servicio (*churn*).  
Se parte de un dataset con información demográfica, contractual y de consumo, y se aplican **técnicas de preprocesamiento, balanceo de clases, escalado y modelado** utilizando distintos algoritmos de Machine Learning.

---

## 🛠️ Tecnologías Utilizadas  
- **Lenguaje:** Python 3.x  
- **Librerías Principales:**
  - `pandas`, `numpy` → Manipulación y análisis de datos.
  - `matplotlib`, `seaborn` → Visualización de datos.
  - `scikit-learn` → Modelado predictivo y preprocesamiento.
  - `imbalanced-learn` → Técnicas de balanceo de clases (SMOTE, undersampling).

---

## 📂 Flujo de Trabajo  

### 1. **Carga y Limpieza de Datos**  
- Eliminación de columnas irrelevantes (`customerID`).
- Imputación de valores nulos en `account_Charges_Total` con la media.
- Conversión de variables categóricas mediante **One-Hot Encoding**.

### 2. **Análisis Exploratorio (EDA)**  
- Distribución de la variable objetivo (`Churn`).
- Relación entre churn y variables como:
  - Tipo de contrato.
  - Antigüedad del cliente.
  - Cargos mensuales y totales.
  - Servicios adicionales.
- Correlaciones y mapa de calor para identificar relaciones relevantes.

### 3. **Preprocesamiento y Balanceo**  
- Separación en conjuntos de **entrenamiento y prueba** con estratificación.
- Balanceo de clases con:
  - **SMOTE** (oversampling sintético).
  - **RandomUnderSampler** (undersampling).
- Escalado de variables continuas con **StandardScaler** (para modelos sensibles a la escala).

### 4. **Modelado Predictivo**  
- **Regresión Logística** (interpretabilidad y coeficientes).
- **Random Forest** (mejor rendimiento general y manejo de datos no escalados).
- Comparación de métricas:
  - Accuracy, Precision, Recall, F1-Score.
  - Matrices de confusión.

### 5. **Interpretación de Resultados**  
- Identificación de variables con mayor impacto en el churn.
- Comparación entre importancia de características (Random Forest) y coeficientes (Logística).

---

## 📈 Principales Resultados  

**Top 5 Predictores de Churn:**
1. Contrato mes a mes.
2. Antigüedad menor a 6 meses.
3. Falta de servicio de seguridad en línea.
4. Uso de facturación electrónica.
5. Cargos mensuales altos.

**Rendimiento de Modelos:**
| Modelo               | Accuracy | Recall (Churn) | Precisión (Churn) | F1-Score |
|----------------------|----------|----------------|-------------------|----------|
| Regresión Logística  | 75.3%    | 59.8%          | 50.2%             | 54.6%    |
| **Random Forest**    | **79.8%**| **70.4%**      | **55.1%**         | **61.8%**|

---

## 🎯 Recomendaciones Estratégicas  
1. **Incentivar contratos anuales** con descuentos.
2. **Paquetes con seguridad incluida** en los primeros meses.
3. **Programa de onboarding** para nuevos clientes.
4. **Facturación personalizada** para aumentar engagement.
5. **Revisión de precios** para clientes de alto consumo.

---

## 🚀 Próximos Pasos  
- Implementar un sistema de **alerta temprana** con Random Forest.
- Realizar **pilotos controlados** para validar estrategias de retención.
- Monitorear impacto en:
  - Reducción de tasa de churn.
  - Conversión a contratos largos.
  - Adopción de servicios adicionales.

---

## 📜 Licencia  
Este proyecto es de uso educativo y libre para análisis y replicación.
