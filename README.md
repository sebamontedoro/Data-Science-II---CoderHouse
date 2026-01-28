# 📈 Análisis Integral de Riesgo y Retorno: Alpha Capital Investments

**Curso:** Data Science II - CoderHouse  
**Autor:** Victorio Montedoro  
**Período:** Noviembre 2025 - Enero 2026

---

## 📋 Descripción del Proyecto

Este proyecto simula un encargo de consultoría para el fondo de inversión ficticio **"Alpha Capital Investments"**.

El objetivo principal es resolver el dilema de los inversores conservadores: **¿Cómo capturar el crecimiento explosivo del sector tecnológico sin exponer el patrimonio a riesgos inaceptables?**

El proyecto se desarrolló en dos fases:

| Fase | Descripción | Enfoque |
|:-----|:------------|:--------|
| **Primer Entregable** | Análisis Exploratorio de Datos (EDA) | Análisis descriptivo, correlaciones, drawdowns |
| **Entrega Final** | Machine Learning Predictivo | Clasificación de regímenes Bull/Bear |

---

## 🎯 Objetivos

### Primer Entregable (EDA)
1. **Validación de Hipótesis:** Determinar si la volatilidad del sector tecnológico justifica sus retornos
2. **Análisis de Resiliencia:** Cuantificar el "dolor" del inversor mediante *Maximum Drawdown*
3. **Estrategia de Diversificación:** Encontrar correlaciones óptimas para un portafolio "Barbell"

### Entrega Final (Machine Learning)
1. **Predicción de Regímenes:** Clasificar si el mercado estará en fase Bull (alcista) o Bear (bajista)
2. **Ingeniería de Features:** Crear indicadores técnicos predictivos (RSI, MACD, Bollinger, etc.)
3. **Optimización de Modelos:** Encontrar el mejor modelo mediante GridSearch y validación cruzada temporal

---

## 📊 Dataset

| Aspecto | Primer Entregable | Entrega Final |
|:--------|:------------------|:--------------|
| **Período** | 5 años | **15 años** |
| **Activos Alto Riesgo** | NVDA, AAPL, MSFT | + TSLA, AMD |
| **Activos Defensivos** | KO, WMT | + PG, JNJ |
| **Total Activos** | 6 | **10** |
| **Fuente** | Yahoo Finance API | Yahoo Finance API |

### Activos Analizados

**🔴 Alto Riesgo (Tecnología):**
- NVDA (Nvidia)
- TSLA (Tesla)
- AMD (Advanced Micro Devices)
- AAPL (Apple)
- MSFT (Microsoft)

**🟢 Bajo Riesgo (Defensivos):**
- KO (Coca-Cola)
- WMT (Walmart)
- PG (Procter & Gamble)
- JNJ (Johnson & Johnson)

**📊 Benchmark:**
- ^GSPC (S&P 500)

---

## 📊 Hallazgos Clave

### Del Análisis Exploratorio (EDA)

> *"La diversificación no se trata de comprar muchas acciones, sino de comprar acciones que no se muevan igual."*

- **Riesgo vs. Retorno:** NVIDIA mostró crecimiento exponencial pero con volatilidad 3x superior al consumo defensivo
- **El Factor de Miedo:** Drawdowns superiores al 60% en tecnología vs. menos del 15% en defensivos
- **Correlación Cero:** Se descubrió correlación cercana a cero entre NVDA y KO, validando la estrategia Barbell

### Del Modelo de Machine Learning

- **Problema:** Clasificación binaria (Bull vs Bear) con horizonte de 1 semana
- **Features Más Predictivas:** Momentum (retornos recientes), volatilidad, RSI, spreads entre grupos de riesgo
- **Modelos Evaluados:** Logistic Regression, Random Forest, XGBoost
- **Validación:** TimeSeriesSplit (5 folds) para respetar el orden temporal

---

## 🗂 Estructura del Repositorio

```
📁 Data-Science-II---CoderHouse/
│
├── 📄 README.md                          # Este archivo
├── 📄 requirements.txt                   # Dependencias del proyecto
│
├── 📁 Primer_Entregable/
│   ├── 📓 Victorio_Montedoro_..._Primer_Entregable.ipynb
│   ├── 📄 Reporte_Ejecutivo_AlphaCapital.pdf
│   └── 💾 datos_precios.csv              # 5 años, 6 activos
│
└── 📁 Entrega_Final/
    ├── 📓 Victorio_Montedoro_..._Entrega_Final.ipynb
    ├── 🤖 mejor_modelo_regimen.pkl       # Modelo entrenado
    └── 🔧 scaler.pkl                     # Scaler para normalización
```

### Descripción de Archivos

| Archivo | Descripción |
|:--------|:------------|
| `Primer_Entregable/*.ipynb` | Notebook con EDA, visualizaciones y análisis de correlación |
| `Primer_Entregable/*.pdf` | Reporte ejecutivo para gerencia (sin código) |
| `Primer_Entregable/*.csv` | Dataset procesado del primer análisis |
| `Entrega_Final/*.ipynb` | Notebook con pipeline completo de ML |
| `Entrega_Final/*.pkl` | Modelo y scaler guardados para predicciones futuras |

---

## 🛠 Tecnologías Utilizadas

### Lenguaje
- **Python 3.10+**

### Librerías

| Categoría | Librerías |
|:----------|:----------|
| **Datos** | `pandas`, `numpy`, `yfinance` |
| **Visualización** | `matplotlib`, `seaborn` |
| **Machine Learning** | `scikit-learn`, `xgboost` |
| **Interpretabilidad** | `shap` |
| **Estadística** | `scipy.stats` |

---

## 🚀 Instalación y Uso

### 1. Clonar el repositorio

```bash
git clone https://github.com/sebamontedoro/Data-Science-II---CoderHouse.git
cd Data-Science-II---CoderHouse
```

### 2. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 3. Ejecutar los Notebooks

**Opción A: Google Colab (Recomendado)**
- Subir los notebooks a Colab
- Ejecutar las celdas secuencialmente

**Opción B: Jupyter Notebook Local**
```bash
jupyter notebook
```

**Opción C: VS Code**
- Abrir la carpeta del proyecto
- Instalar extensión de Jupyter
- Ejecutar los notebooks

---

## 📈 Resultados del Modelo

| Modelo | AUC-ROC | Accuracy | F1-Score |
|:-------|:--------|:---------|:---------|
| Logistic Regression | - | - | - |
| Random Forest (Optimizado) | - | - | - |
| XGBoost (Optimizado) | - | - | - |

> **Nota:** Los valores específicos se generan al ejecutar el notebook con datos actualizados.

---

## 🔮 Próximos Pasos

1. **Ensemble de Modelos:** Combinar predicciones para mayor robustez
2. **Backtest Financiero:** Simular estrategia de trading real
3. **Features de Sentiment:** Incorporar análisis de noticias y redes sociales
4. **Deep Learning:** Explorar LSTM para dependencias temporales complejas

---

## 📚 Referencias

- [Yahoo Finance API (yfinance)](https://pypi.org/project/yfinance/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [SHAP Values Explained](https://shap.readthedocs.io/)

---

## 👤 Autor

**Victorio Montedoro**

---

## 📄 Licencia

Este proyecto fue realizado con fines académicos como parte del curso **Data Science II de CoderHouse**.

*Noviembre 2025 - Enero 2026*