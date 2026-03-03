# Evaluación Predictiva de Precipitaciones Pluviales (CDMX) 🌧️

Este proyecto integra datos climáticos de **CONAGUA/SMN**, niveles de radiación solar y contaminantes ambientales para analizar e identificar patrones que influyen en las lluvias a escala regional (Ciudad de México).

## 📊 Descripción del Proyecto
El objetivo principal es predecir la ocurrencia de precipitación (binarizada > 0) utilizando modelos de Machine Learning y Deep Learning, evaluando el impacto de variables como la temperatura media, radiación y partículas contaminantes.

## 🛠️ Herramientas Utilizadas
- **Lenguaje:** Python (Google Colab)
- **Librerías principales:**
  - `Pandas` & `Numpy`: Procesamiento y limpieza de datos.
  - `Scikit-Learn`: Modelos clásicos y métricas de evaluación.
  - `XGBoost`: Modelo de Gradient Boosting.
  - `TensorFlow/Keras`: Red Neuronal **LSTM** para series temporales.
  - `Folium`: Visualización geográfica de estaciones.

## 📈 Metodología
1. **Integración:** Fusión de datasets por fecha y ubicación.
2. **Manejo de Gaps:** Se aplicó **interpolación lineal** para completar datos faltantes.
3. **Feature Engineering:** Creación de lags temporales, variables polinómicas y promedios regionales por municipio.
4. **Split Temporal:** Entrenamiento con datos hasta 2019 y validación con datos de 2020+.

## 🏆 Resultados y Conclusiones
Se evaluaron 4 modelos principales:
- Regresión Logística
- Random Forest
- **XGBoost** (Mejor desempeño en F1-Score)
- LSTM

**Insight Clave:** El modelo **XGBoost** demostró mayor precisión para este conjunto de datos tabulares. Los contaminantes (PM) mostraron una correlación no lineal con la lluvia, sugiriendo que actúan como núcleos de condensación bajo condiciones térmicas específicas.

---
**Autor:** Amairani Citlali Ramos Aguilar  
**Institución:** UNAM
