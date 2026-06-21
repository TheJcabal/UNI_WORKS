<div align="center">

<img src="assets/logo_unipacifico.png" alt="Logo Universidad del Pacífico" width="180">

# 📊 Taller Práctico No. 4 — NumPy, Matplotlib y Seaborn

### Universidad del Pacífico

**Programa de Ingeniería de Sistemas**
**Asignatura:** Inteligencia Artificial
**Docente:** Wilman Andrés Quiñonez V.
**Semestre VIII — Corte II**

## Caso de estudio

### Predicción de Rotación de Empleados en una Empresa Tecnológica

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?logo=numpy)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Graphics-5B8DB8)

</div>

---

# 👥 Integrantes

* Ángel Santiago Estupiñán Gómez
* Stefany Potosí
* Cristian Valderrama
* Ewdar Suárez
* Steven Cabal

---

# 📌 Descripción

Este repositorio contiene el desarrollo del **Taller Práctico No. 4**, enfocado en la aplicación de las librerías **NumPy**, **Matplotlib** y **Seaborn** dentro de un flujo típico de análisis de datos e Inteligencia Artificial.

El proyecto comprende:

* Generación de datos sintéticos.
* Estadística descriptiva mediante NumPy.
* Visualización de datos con Matplotlib.
* Análisis exploratorio utilizando Seaborn.
* Interpretación de resultados y formulación de conclusiones y recomendaciones.

Todo el desarrollo se encuentra implementado en el notebook:

```text
taller4_caso1.ipynb
```

Compatible con:

* Jupyter Notebook
* Google Colab
* Visual Studio Code + Jupyter

---

# 🎯 Objetivo General

Aplicar las librerías **NumPy**, **Matplotlib** y **Seaborn** al procesamiento, análisis estadístico y visualización de un conjunto de datos sintético relacionado con la rotación de empleados, con el fin de identificar patrones y relaciones que apoyen la toma de decisiones empresariales.

---

# 📂 Estructura del repositorio

```text
taller_practico_librerias_numpy_matplotlib_seaborn/
│
├── taller4_caso1.ipynb
├── README.md
└── assets/
    └── logo_unipacifico.png
```

---

# 📚 Contenido del Proyecto

## Parte I — Investigación y ejercicios guía

### NumPy

* Indexación de matrices.
* Operaciones estadísticas.
* Generación de datos aleatorios.
* Distribuciones normales.

### Matplotlib

* Gráficos de líneas.
* Histogramas.
* Gráficos de barras.

### Seaborn

* Heatmap de correlaciones.
* Boxplots.
* Pairplots.
* Análisis exploratorio.

---

# 🏢 Caso de estudio

## Predicción de Rotación de Empleados

Una empresa de desarrollo de software busca comprender los factores asociados a la renuncia de sus colaboradores para implementar estrategias de retención.

Se construyó un conjunto de datos sintético de **500 empleados** con las siguientes variables:

| Variable        | Descripción                  |
| --------------- | ---------------------------- |
| Edad            | Edad del empleado            |
| Salario Mensual | Ingreso mensual              |
| Horas Extras    | Horas extras por mes         |
| Antigüedad      | Tiempo en la empresa         |
| Satisfacción    | Nivel de satisfacción (1-10) |
| Renunció        | Sí / No                      |

La variable de renuncia fue generada mediante una función logística para representar un comportamiento cercano a situaciones reales.

---

# 📈 Visualizaciones desarrolladas

### Matplotlib

1. Histograma de salarios.
2. Distribución de renuncias.
3. Relación entre salario y satisfacción.

### Seaborn

4. Heatmap de correlación.
5. Boxplot de salarios según renuncia.
6. Pairplot de variables numéricas.

---

# 🔍 Hallazgos principales

* La satisfacción laboral es la variable más relacionada con la rotación.
* El incremento de horas extras afecta negativamente la satisfacción.
* La antigüedad disminuye la probabilidad de renuncia.
* El salario, por sí solo, presenta una relación débil con la rotación.
* No se observaron problemas importantes de multicolinealidad.

---

# ✅ Conclusiones

1. La satisfacción laboral constituye el principal factor asociado con la renuncia.
2. El exceso de horas extras incrementa el riesgo de rotación.
3. La antigüedad favorece la permanencia de los empleados.
4. Las estrategias basadas únicamente en aumentos salariales serían insuficientes.
5. El conjunto de datos puede utilizarse posteriormente para construir modelos predictivos.

---

# 💡 Recomendaciones

* Monitorear la carga laboral y las horas extras.
* Realizar mediciones periódicas de satisfacción laboral.
* Implementar programas de acompañamiento para empleados nuevos.
* Desarrollar sistemas predictivos para apoyar la gestión del talento humano.

---

# 🤖 Relación con la Inteligencia Artificial

El análisis exploratorio desarrollado constituye una etapa previa para la construcción de modelos de Machine Learning, como:

* Regresión Logística.
* Árboles de Decisión.
* Random Forest.

Estos modelos permitirían estimar la probabilidad de renuncia y apoyar la toma de decisiones en las áreas de Gestión Humana.

---

# ⚙️ Instalación

```bash
pip install numpy pandas matplotlib seaborn
```

---

# ▶️ Ejecución

1. Abrir `taller4_caso1.ipynb`.
2. Ejecutar todas las celdas.
3. Analizar los resultados obtenidos.

---

# 🛠 Tecnologías Utilizadas

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# 📄 Autoría

Trabajo desarrollado como entrega del **Taller Práctico No. 4** de la asignatura **Inteligencia Artificial**, correspondiente al **Semestre VIII – Corte II**, del programa de **Ingeniería de Sistemas de la Universidad del Pacífico**, bajo la orientación del docente **Wilman Andrés Quiñonez V.**

---

<div align="center">

### Universidad del Pacífico

**Ingeniería de Sistemas · 2026**

</div>
