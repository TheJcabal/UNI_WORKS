# Algoritmos de Búsqueda en Grafos: BFS y DFS

Este repositorio contiene un ejercicio práctico diseñado para ejecutarse en **Google Colab**, cuyo objetivo es comprender e implementar los dos algoritmos fundamentales de recorrido de grafos: **Búsqueda en Anchura (BFS)** y **Búsqueda en Profundidad (DFS)** utilizando el lenguaje **Python**.

## 📖 Introducción

Los algoritmos de búsqueda son la base para resolver problemas complejos en ciencias de la computación, desde la navegación GPS hasta la inteligencia artificial en videojuegos. Este proyecto se centra en las dos estrategias principales de exploración:

1.  **BFS (Breadth-First Search - Búsqueda en Anchura):** Explora el grafo nivel por nivel.
2.  **DFS (Depth-First Search - Búsqueda en Profundidad):** Explora el grafo avanzando tanto como sea posible por cada rama antes de retroceder.

## 🎯 Objetivos del Ejercicio

Basado en la actividad propuesta, este cuaderno de trabajo busca cumplir con las siguientes metas:

1.  **Implementación:** Desarrollar la lógica de BFS y DFS en Python para recorrer un grafo pequeño definido manualmente.
2.  **Análisis Comparativo:** Ejecutar ambos algoritmos sobre el mismo grafo para observar las diferencias en:
    *   **El camino encontrado:** ¿En qué orden se visitan los nodos?
    *   **El uso de memoria:** ¿Qué estructura de datos requiere cada uno?

## 🧠 Conceptos Clave

Para entender el código incluido en el cuaderno, es importante tener claros los siguientes conceptos teóricos:

### Búsqueda en Anchura (BFS)
*   **Estrategia:** "Inundación" o capas de cebolla. Comienza en un nodo raíz y visita todos los vecinos directos antes de pasar a los vecinos de segundo nivel.
*   **Estructura de Datos:** Utiliza una **Cola (Queue)** bajo el principio FIFO (First In, First Out).
*   **Aplicación ideal:** Encontrar la ruta más corta en grafos no ponderados (menor número de saltos).

### Búsqueda en Profundidad (DFS)
*   **Estrategia:** "Laberinto". Avanza por un camino hasta que no tiene salida, luego retrocede (*backtracking*) hasta la última bifurcación y prueba un camino diferente.
*   **Estructura de Datos:** Utiliza una **Pila (Stack)** (principio LIFO) o **Recursividad** (pila de llamadas del sistema).
*   **Aplicación ideal:** Explorar todas las posibilidades, soluciones de rompecabezas, detección de ciclos o componentes conectados.

## 📊 Comparación de Resultados

En el cuaderno de Google Colab, se analizarán los resultados bajo dos criterios principales:

*   **Camino Encontrado:** Se observará cómo BFS garantiza encontrar el nodo objetivo en la menor cantidad de pasos (niveles), mientras que DFS puede encontrar el objetivo muy rápido o tardar mucho dependiendo de la "suerte" al elegir la primera rama, pero no garantiza el camino más corto.
*   **Memoria Usada:** Se discutirá cómo BFS puede consumir mucha memoria si el grafo es muy ancho (muchos vecinos), mientras que DFS es generalmente más eficiente en memoria, a menos que el grafo sea extremadamente profundo.

## 🚀 Instrucciones de Uso

1.  Descarga el archivo `.ipynb` de este repositorio o ábrelo directamente mediante el enlace a Google Colab.
2.  Ejecuta las celdas secuencialmente.
3.  Observa la definición del grafo (nodos y aristas).
4.  Ejecuta las funciones de búsqueda y compara las salidas de texto para ver el orden de visita de los nodos.
5.  Lee las conclusiones al final del cuaderno.
