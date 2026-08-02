# 📊 Taller 3 — Análisis Estadístico Descriptivo y Visualización de Datos

<p align="center">
  <img src="https://img.shields.io/badge/Universidad%20del%20Pac%C3%ADfico-Ing.%20de%20Sistemas-1a6b3c?style=for-the-badge" alt="Universidad del Pacífico"/>
  <img src="https://img.shields.io/badge/Asignatura-Inteligencia%20Artificial-0077b6?style=for-the-badge" alt="Inteligencia Artificial"/>
  <img src="https://img.shields.io/badge/Semestre-8%20%E2%80%94%20Corte%20II-f4a261?style=for-the-badge" alt="Semestre 8"/>
  <img src="https://img.shields.io/badge/Herramientas-Excel%20%7C%20Python-8ecae6?style=for-the-badge" alt="Excel | Python"/>
</p>

---

## 📌 Descripción

Este repositorio contiene el desarrollo completo del **Taller No. 3** de la asignatura de Inteligencia Artificial. El objetivo principal es aplicar técnicas de **estadística descriptiva** para transformar datos en información útil, usando tablas de distribución de frecuencias, gráficos estadísticos e interpretación cuantitativa de resultados.

El análisis se centra en la variable **"Apps Descargadas"**, extraída de un conjunto de datos que simula el comportamiento de usuarios de aplicaciones móviles.

---

## 🎯 Competencias Desarrolladas

- Identificación de variables y características del conjunto de datos.
- Construcción de tablas de distribución de frecuencias.
- Representación de datos mediante gráficos estadísticos (histograma, polígono de frecuencias y ojiva).
- Análisis e interpretación del comportamiento de los datos con evidencia cuantitativa.

---

## 🗂️ Estructura del Repositorio

```
Taller-3/
├── Taller-3.xlsx                               # Dataset y tabla de frecuencias (archivo fuente)
├── Taller_analisis_estadistico_frecuencia.pdf  # Enunciado oficial del taller
├── Taller3_C2.pdf                              # Informe técnico entregable (PDF)
└── README.md                                   # Este archivo
```

---

## 📂 Descripción del Dataset

| Aspecto                          | Descripción                           |
|----------------------------------|---------------------------------------|
| **Población**                    | Usuarios de aplicaciones móviles      |
| **Muestra**                      | 50 observaciones                      |
| **Unidad de análisis**           | Cada usuario registrado               |
| **Variable analizada**           | Apps Descargadas                      |
| **Tipo de variable**             | Cuantitativa continua                 |

---

## 🔢 Cálculos Estadísticos Principales

| Parámetro                             | Valor                        |
|---------------------------------------|------------------------------|
| **Valor mínimo**                      | 30                           |
| **Valor máximo**                      | 132                          |
| **Rango**                             | 102                          |
| **Número de clases (Regla de Sturges)** | 7                          |
| **Amplitud de clase**                 | 15 (redondeado de 14,57)     |
| **Total de observaciones (n)**        | 50                           |

> **Regla de Sturges aplicada:**  
> `k = 1 + 3.322 × log₁₀(n) = 1 + 3.322 × log₁₀(50) ≈ 6.64 → 7 intervalos`

---

## 📋 Tabla de Distribución de Frecuencias

| Intervalo    | Marca de clase (Xᵢ) | Frec. Absoluta (fᵢ) | Frec. Relativa (hᵢ) | Frec. Acumulada (Fᵢ) | Frec. Rel. Acumulada (Hᵢ) |
|--------------|---------------------|---------------------|---------------------|----------------------|---------------------------|
| [30 – 45)    | 37,5                | 7                   | 14,00 %             | 7                    | 14,00 %                   |
| [45 – 60)    | 52,5                | 6                   | 12,00 %             | 13                   | 26,00 %                   |
| [60 – 75)    | 67,5                | **10**              | **20,00 %**         | 23                   | 46,00 %                   |
| [75 – 90)    | 82,5                | 9                   | 18,00 %             | 32                   | 64,00 %                   |
| [90 – 105)   | 97,5                | 8                   | 16,00 %             | 40                   | 80,00 %                   |
| [105 – 120)  | 112,5               | 5                   | 10,00 %             | 45                   | 90,00 %                   |
| [120 – 135]  | 127,5               | 5                   | 10,00 %             | 50                   | 100,00 %                  |
| **Total**    |                     | **50**              | **100,00 %**        |                      |                           |

---

## 📈 Representación Gráfica

Se construyeron tres gráficos estadísticos a partir de la tabla de frecuencias:

### 📊 Histograma de Frecuencias
Muestra la distribución de la variable por intervalos. El intervalo **[60 – 75)** presenta la mayor barra, lo que confirma que es el de mayor concentración de observaciones.

### 📉 Polígono de Frecuencias
Une los puntos medios (marcas de clase) con sus respectivas frecuencias absolutas. La curva asciende desde el primer intervalo hasta su punto máximo en la marca de clase **67,5**, y luego desciende progresivamente, revelando la forma de la distribución.

### 📐 Ojiva (Curva Acumulada)
Representa las frecuencias relativas acumuladas. Permite estimar rápidamente qué porcentaje de usuarios se encuentra por debajo de un valor determinado:

- **14 %** de los usuarios descargó menos de **45 apps**
- **46 %** descargó menos de **75 apps**
- **64 %** descargó menos de **90 apps**
- **80 %** descargó menos de **105 apps**

---

## 🔍 Análisis e Interpretación

**1. ¿Cuál es el intervalo con mayor concentración?**  
El intervalo **[60 – 75)** agrupa 10 de los 50 usuarios (20 %), siendo el de mayor frecuencia.

**2. ¿La distribución es uniforme, normal o sesgada?**  
La distribución no es uniforme. Presenta una concentración central con tendencia aproximada a la normalidad, aunque con un ligero sesgo hacia los valores más bajos. No es perfectamente simétrica, pero sí muestra el patrón de campana típico.

**3. ¿Qué porcentaje está por debajo de cierto nivel de descargas?**  
Según la ojiva: el 46 % descargó menos de 75 apps, el 64 % menos de 90 y el 80 % menos de 105.

**4. ¿Qué información aporta la ojiva para la toma de decisiones?**  
Permite identificar umbrales de comportamiento de usuarios. Por ejemplo, para diseñar estrategias diferenciadas entre usuarios con baja, media y alta actividad de descarga.

**5. ¿Qué conclusiones se obtienen del análisis general?**  
La mayoría de los usuarios tiene un perfil de descargas moderado, concentrado entre 60 y 105 apps. Los usuarios con muy pocas (< 45) o muchas descargas (> 105) representan la minoría.

---

## 📝 Conclusiones Finales

El análisis estadístico descriptivo aplicado a la variable **"Apps Descargadas"** permitió:

- Organizar 50 observaciones en 7 intervalos de clase con una amplitud de 15 unidades.
- Identificar que el rango de datos es amplio (102 unidades), evidenciando diversidad de comportamientos entre usuarios.
- Confirmar que la distribución tiene una forma aproximadamente acampanada, con el pico en el intervalo [60 – 75).
- Determinar mediante la ojiva que el 80 % de los usuarios descarga menos de 105 apps, información útil para la segmentación de usuarios.

En conjunto, el taller demostró que el análisis estadístico descriptivo no se limita a realizar cálculos: su valor real está en la capacidad de interpretar los resultados y convertirlos en información accionable para la toma de decisiones.

---

## 👤 Información del Estudiante

| Campo        | Detalle                             |
|--------------|-------------------------------------|
| **Estudiante** | Jheison Estiben Cabal Chimbaco    |
| **Docente**    | Wilman Andrés Quiñonez V.         |
| **Universidad** | Universidad del Pacífico         |
| **Programa**   | Ingeniería de Sistemas            |
| **Asignatura** | Inteligencia Artificial           |
| **Semestre**   | 8 — Corte II — 2026               |
| **Ciudad**     | Buenaventura, Valle del Cauca     |

---

<p align="center">
  <sub>Elaborado con fines académicos · Universidad del Pacífico · 2026</sub>
</p>
