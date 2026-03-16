# 🔎 BFS y DFS en Grafos

Implementación y comparación de dos algoritmos clásicos de búsqueda en grafos:

- **BFS (Breadth-First Search)** → búsqueda en anchura
- **DFS (Depth-First Search)** → búsqueda en profundidad

Estos algoritmos son fundamentales en el estudio de estructuras de datos, inteligencia artificial y teoría de grafos.

---

# 🚀 Ejecutar en Google Colab

Puedes ejecutar el notebook directamente en Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TheJcabal/UNI_WORKS/blob/main/AI/BFS_DFS/DFS_DFS.ipynb)

---

# 📖 Descripción

Este proyecto muestra cómo funcionan los algoritmos de búsqueda en grafos utilizando Python.

Se incluyen:

- explicación teórica
- implementación en Python
- ejemplos prácticos
- visualización del recorrido en el grafo

---

# 🧠 Algoritmos incluidos

## BFS — Breadth First Search

Explora el grafo **nivel por nivel**, visitando primero todos los nodos vecinos antes de avanzar al siguiente nivel.

Características:

- usa una **cola (queue)**
- encuentra el camino más corto en grafos no ponderados

Aplicaciones:

- redes sociales
- sistemas de navegación
- búsqueda de rutas

---

## DFS — Depth First Search

Explora el grafo **profundizando lo máximo posible** antes de retroceder.

Características:

- usa **pila (stack)** o recursividad
- útil para recorrer estructuras complejas

Aplicaciones:

- detección de ciclos
- análisis de grafos
- resolución de laberintos

---

# 🛠 Tecnologías utilizadas

- Python
- Google Colab
- Jupyter Notebook
- Grafos

---

# 👨‍💻 Autor

**Steven / Jheison Cabal**

Repositorio académico con proyectos y tareas universitarias.# BFS y DFS en un grafo

## Descripcion
Este ejemplo compara dos metodos de busqueda en grafos:

- BFS (Breadth-First Search): explora por niveles.
- DFS (Depth-First Search): explora en profundidad.

El script imprime el orden de visita en consola y muestra una visualizacion para diferenciar ambos recorridos.

## Archivo principal
- `bfs_dfs.py`

## Requisitos
- Python 3.8 o superior
- matplotlib
- networkx

## Instalacion
```bash
python3 -m pip install matplotlib networkx
```

## Ejecucion
Desde la carpeta `carpeta/Work_Uni`:

```bash
python3 bfs_dfs.py
```

## Salida esperada
En consola se imprime algo similar a:

```text
Busqueda BFS:
A -> B -> C -> D -> E -> F

Busqueda DFS:
A -> B -> D -> E -> F -> C
```

Y en pantalla se abre una figura con 3 paneles:

1. Grafo original.
2. Recorrido BFS.
3. Recorrido DFS.

## Como leer la grafica
- Aristas grises: conexiones originales del grafo.
- Aristas coloreadas: aristas usadas por el recorrido.
- Numero en cada nodo: orden de visita.

## Personalizacion rapida
- Cambia el contenido del diccionario `grafo` para probar otros casos.
- Cambia el nodo inicial en las lineas donde se llama a `bfs(grafo, 'A')` y `dfs(grafo, 'A')`.

## Problemas comunes
Si aparece un error de importacion, instala las dependencias:

```bash
python3 -m pip install matplotlib networkx
```
