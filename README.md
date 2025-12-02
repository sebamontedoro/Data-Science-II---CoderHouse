# 📈 Análisis Integral de Riesgo y Retorno: Alpha Capital Investments

**Curso:** Data Science II - CoderHouse 
**Periodo de Análisis:** Último Año (12 Meses)

-----

## 📋 Descripción del Proyecto

Este proyecto simula un encargo de consultoría para el fondo de inversión ficticio **"Alpha Capital Investments"**.

El objetivo principal es resolver el dilema de los inversores conservadores: **¿Cómo capturar el crecimiento explosivo del sector tecnológico sin exponer el patrimonio a riesgos inaceptables?**

Utilizando datos históricos de **Yahoo Finance**, analizamos el comportamiento de gigantes tecnológicos (**NVIDIA, Apple, Microsoft**) frente a activos de refugio (**Coca-Cola, Walmart**) para diseñar una estrategia de diversificación matemáticamente eficiente en el corto plazo.

## 🎯 Objetivos

1.  **Validación de Hipótesis:** Determinar si la volatilidad del sector tecnológico justifica sus retornos a corto plazo.
2.  **Análisis de Resiliencia:** Cuantificar el "dolor" del inversor mediante el cálculo de *Maximum Drawdown* (caída máxima).
3.  **Estrategia de Inversión:** Encontrar la correlación óptima entre activos para proponer un portafolio "Barbell".

## 📊 Hallazgos Clave (Insights)

> *"La diversificación no se trata de comprar muchas acciones, sino de comprar acciones que no se muevan igual."*

  * **Riesgo vs. Retorno:** NVIDIA ha mostrado un crecimiento exponencial, pero con una volatilidad muy superior al consumo masivo.
  * **El Factor de Miedo (Drawdown):** Invertir en tecnología requiere estómago; se observaron caídas significativas en periodos de corrección, mientras que Coca-Cola actuó como amortiguador.
  * **La Joya Oculta:** Se descubrió una **correlación cercana a cero** entre Coca-Cola y NVIDIA. Esto valida matemáticamente que combinarlas reduce el riesgo sistémico del portafolio.

## 🗂 Estructura del Repositorio

Este repositorio contiene todos los entregables del proyecto:

| Archivo | Tipo | Descripción |
| :--- | :--- | :--- |
| `Victorio Montedoro - Ciencia de datos II - Primer Entregable.ipynb` | 📓 **Notebook** | El núcleo del proyecto. Contiene la extracción de datos (API), limpieza, EDA, cálculos financieros y conclusiones. |
| `Reporte_Ejecutivo_AlphaCapital.pdf` | 📄 **Informe** | Documento formal para la gerencia. Resume los hallazgos sin código, enfocado en la toma de decisiones. |
| `datos_precios.csv` | 💾 **Data** | Dataset procesado con 1 año de historia de precios ajustados. |

## 🛠 Tecnologías Utilizadas

El proyecto fue desarrollado íntegramente en **Python** utilizando las siguientes librerías:

  * **Extracción de Datos:** `yfinance` (Yahoo Finance API)
  * **Manipulación de Datos:** `pandas`, `numpy`
  * **Visualización:** `matplotlib`, `seaborn`
  * **Estadística:** `scipy.stats`
  * **Generación de Reportes:** `reportlab` (PDF), `python-pptx` (PowerPoint)

## 🚀 Instalación y Uso

Para replicar este análisis en tu entorno local:

1.  **Clonar el repositorio:**

    ```bash
    git clone [https://github.com/sebamontedoro/Data-Science-II.git](https://github.com/sebamontedoro/Data-Science-II.git)
    ```

2.  **Instalar dependencias:**

    ```bash
    pip install pandas yfinance matplotlib seaborn scipy reportlab python-pptx
    ```

3.  **Ejecutar el Notebook:**
    Abre `Entrega_Final_DS.ipynb` en Jupyter Notebook, Google Colab o VS Code y ejecuta las celdas secuencialmente.

-----

### 👤 Autor

**Victorio Montedoro**

-----

*Este proyecto fue realizado con fines académicos como parte de la cursada de Data Science II de CoderHouser, durante Noviembre de 2025.*
