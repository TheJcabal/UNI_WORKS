# Taller Práctico No. 4 — NumPy, Matplotlib y Seaborn

**Universidad del Pacífico — Programa de Ingeniería de Sistemas**
**Asignatura:** Inteligencia Artificial
**Semestre 8 — Corte II**
**Caso de estudio desarrollado:** Caso 1 — Predicción de Rotación de Empleados en una Empresa Tecnológica

## 1. Descripción general

Este repositorio contiene el desarrollo completo del Taller Práctico No. 4, el cual integra el uso de las librerías NumPy, Matplotlib y Seaborn dentro del flujo típico de un proyecto de Inteligencia Artificial: generación de datos sintéticos, cálculo de estadísticos descriptivos, visualización de datos y análisis exploratorio orientado a la toma de decisiones.

El trabajo se desarrolla en su totalidad dentro del notebook `taller4_caso1.ipynb`, ejecutable de inicio a fin en Jupyter Notebook o Google Colab, y se complementa con este documento README, que resume la metodología, los hallazgos y las conclusiones del ejercicio.

## 2. Estructura del repositorio

```
taller_practico_librerias_numpy_matplotlib_seaborn/
├── taller4_caso1.ipynb   # Notebook con el desarrollo completo del taller
└── README.md             # Este documento
```

## 3. Contenido del notebook

### Parte I — Investigación y ejercicios guía

- Respuesta a las trece preguntas conceptuales sobre NumPy, Matplotlib y Seaborn.
- Ejercicios guía de indexación de matrices con NumPy.
- Cálculo de operaciones matemáticas y estadísticas básicas (media, máximo, mínimo, desviación estándar).
- Generación de datos aleatorios con distribución normal y su correspondiente histograma.
- Construcción de un gráfico de líneas (accuracy por época), un histograma, un gráfico de barras, un mapa de calor de correlación y un boxplot, cada uno acompañado de las preguntas de análisis solicitadas en la guía.

### Parte II — Caso de estudio integrador: Rotación de empleados

**Contexto:** una empresa de desarrollo de software desea entender los factores asociados al aumento en la renuncia de su personal, con el fin de diseñar estrategias de retención.

**Generación de datos sintéticos:** se construyó, mediante NumPy, un dataset de 500 empleados con las variables Edad, Salario Mensual, Horas Extras por Mes, Antigüedad en la Empresa, Nivel de Satisfacción (escala 1-10) y Renunció (Sí/No). La variable de renuncia se generó mediante un modelo probabilístico (función logística) en el que la probabilidad de renunciar aumenta cuando la satisfacción es baja y las horas extras son altas, y disminuye con la antigüedad, con el fin de simular un comportamiento realista y no puramente aleatorio.

**Análisis estadístico:** se calcularon la media, la mediana, la desviación estándar de los salarios, la edad promedio y el porcentaje de empleados que renunciaron, utilizando funciones de NumPy.

**Visualización (6 gráficos):**

1. Histograma de salarios mensuales (Matplotlib).
2. Gráfico de barras de la distribución de renuncias (Matplotlib).
3. Gráfico de dispersión entre salario y satisfacción (Matplotlib).
4. Mapa de calor (heatmap) de correlación entre variables numéricas (Seaborn).
5. Boxplot de salarios segmentado por estado de renuncia (Seaborn).
6. Pairplot de todas las variables numéricas, discriminado por estado de renuncia (Seaborn).

Cada gráfico incluye su interpretación individual dentro del notebook.

## 4. Hallazgos principales

- La **satisfacción laboral** es la variable más asociada con la renuncia: los empleados con menores niveles de satisfacción presentan una probabilidad de renuncia notablemente mayor.
- Las **horas extras** se relacionan negativamente con la satisfacción, sugiriendo un posible efecto de sobrecarga laboral que termina derivando en rotación.
- La **antigüedad** actúa como factor protector: a mayor tiempo en la empresa, menor probabilidad de renuncia.
- El **salario**, de forma aislada, no mostró una relación fuerte con la rotación, lo que indica que las estrategias de retención no deberían limitarse a ajustes salariales.
- No se identificó multicolinealidad relevante entre las variables numéricas analizadas.

## 5. Conclusiones

1. La satisfacción laboral es el principal factor explicativo de la rotación detectado en este análisis, por encima del salario.
2. El exceso de horas extras se asocia con una menor satisfacción y, en consecuencia, con un mayor riesgo de renuncia.
3. La antigüedad reduce la probabilidad de abandono, reflejando un efecto de arraigo organizacional.
4. Las estrategias de retención centradas únicamente en el salario tendrían un impacto limitado frente a este fenómeno.
5. El desbalance entre empleados que permanecen y empleados que renuncian debe considerarse al diseñar un futuro modelo predictivo, dado que podría requerir técnicas de balanceo de clases.

## 6. Recomendaciones empresariales

1. Monitorear sistemáticamente la carga de horas extras por empleado, estableciendo alertas tempranas ante cargas excesivas.
2. Implementar mediciones periódicas de satisfacción laboral (encuestas de clima organizacional).
3. Diseñar programas de acompañamiento para empleados de baja antigüedad, segmento con mayor propensión a la rotación según el análisis.

## 7. Reflexión sobre Inteligencia Artificial

El análisis exploratorio desarrollado constituye la base para un futuro modelo de clasificación (regresión logística, árboles de decisión o random forest) que estime la probabilidad de renuncia de cada empleado activo a partir de variables como satisfacción, horas extras y antigüedad. Esto permitiría al área de Gestión Humana priorizar de forma objetiva sus acciones de retención, dirigiendo recursos hacia los colaboradores con mayor riesgo identificado, siempre bajo un uso ético y responsable de la información laboral.

## 8. Cómo ejecutar el notebook

1. Abrir `taller4_caso1.ipynb` en Jupyter Notebook o subirlo a Google Colab.
2. Instalar las dependencias si es necesario: `pip install numpy pandas matplotlib seaborn`.
3. Ejecutar todas las celdas en orden (`Run All`).

## 9. Autoría

Desarrollado como entrega del Taller Práctico No. 4 de la asignatura Inteligencia Artificial, Semestre 8, Corte II, Universidad del Pacífico, Programa de Ingeniería de Sistemas.

Taller original creado por: Wilman Andrés Quiñonez V. — M.Sc. in Data Science | M.Sc. in Applied Artificial Intelligence.
