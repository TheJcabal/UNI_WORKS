```markdown
# Búsqueda en Grafos con Python: BFS y DFS (en Google Colab)

Este repositorio introduce dos métodos clásicos de búsqueda en grafos:

- **BFS (Breadth-First Search)** – Búsqueda en anchura  
- **DFS (Depth-First Search)** – Búsqueda en profundidad  

Usaremos **Python** y ejecutaremos los ejemplos en **Google Colab**.

---

## 1. ¿Qué es un grafo?

Un **grafo** es una estructura formada por:

- **Nodos** (o vértices)
- **Aristas** (conexiones entre nodos)

En Python suele representarse como un **diccionario de listas**, donde cada clave es un nodo y su valor es la lista de nodos vecinos:

```python
grafo = {
    "A": ["B", "C"],
    "B": ["A", "D", "E"],
    "C": ["A", "F"],
    "D": ["B"],
    "E": ["B", "F"],
    "F": ["C", "E"]
}
```

---

## 2. Búsqueda en Anchura (BFS)

**Idea principal:**  
Explora el grafo **nivel por nivel**.  
Primero visita todos los vecinos inmediatos del nodo inicial, luego los vecinos de esos vecinos, y así sucesivamente.

**Se usa típicamente cuando:**

- Quieres encontrar el **camino más corto** (en cantidad de aristas) en grafos no ponderados.
- Quieres saber qué nodos están a cierta “distancia” del nodo inicial.

### 2.1. Algoritmo BFS (resumen)

1. Usar una **cola** (queue).
2. Marcar el nodo inicial como **visitado** y ponerlo en la cola.
3. Mientras la cola no esté vacía:
   - Sacar un nodo de la cola.
   - Visitar todos sus vecinos **no visitados**, marcarlos como visitados y añadirlos a la cola.

### 2.2. Implementación BFS en Python

```python
from collections import deque

def bfs(grafo, inicio):
    visitados = set()
    cola = deque([inicio])
    orden_recorrido = []

    visitados.add(inicio)

    while cola:
        nodo = cola.popleft()
        orden_recorrido.append(nodo)

        for vecino in grafo.get(nodo, []):
            if vecino not in visitados:
                visitados.add(vecino)
                cola.append(vecino)

    return orden_recorrido

# Ejemplo de uso
grafo = {
    "A": ["B", "C"],
    "B": ["A", "D", "E"],
    "C": ["A", "F"],
    "D": ["B"],
    "E": ["B", "F"],
    "F": ["C", "E"]
}

print("Recorrido BFS desde A:", bfs(grafo, "A"))
```

Salida esperada (puede variar según el orden de vecinos):

```text
Recorrido BFS desde A: ['A', 'B', 'C', 'D', 'E', 'F']
```

---

## 3. Búsqueda en Profundidad (DFS)

**Idea principal:**  
Explora el grafo **lo más profundo posible** antes de retroceder.  
Se “sumerge” en una rama hasta que no puede continuar, y luego vuelve atrás (backtracking).

**Se usa típicamente cuando:**

- Quieres comprobar si existe un camino entre dos nodos.
- Quieres explorar todos los nodos alcanzables desde uno inicial.
- Problemas de backtracking, laberintos, etc.

### 3.1. Algoritmo DFS (resumen, versión recursiva)

1. Empezar desde el nodo inicial.
2. Marcar el nodo como **visitado**.
3. Para cada vecino no visitado:
   - Llamar recursivamente a DFS sobre ese vecino.

### 3.2. Implementación DFS (recursiva) en Python

```python
def dfs_recursivo(grafo, inicio, visitados=None, orden_recorrido=None):
    if visitados is None:
        visitados = set()
    if orden_recorrido is None:
        orden_recorrido = []

    visitados.add(inicio)
    orden_recorrido.append(inicio)

    for vecino in grafo.get(inicio, []):
        if vecino not in visitados:
            dfs_recursivo(grafo, vecino, visitados, orden_recorrido)

    return orden_recorrido

# Ejemplo de uso
grafo = {
    "A": ["B", "C"],
    "B": ["A", "D", "E"],
    "C": ["A", "F"],
    "D": ["B"],
    "E": ["B", "F"],
    "F": ["C", "E"]
}

print("Recorrido DFS (recursivo) desde A:", dfs_recursivo(grafo, "A"))
```

---

### 3.3. Implementación DFS (iterativa) con pila

```python
def dfs_iterativo(grafo, inicio):
    visitados = set()
    pila = [inicio]
    orden_recorrido = []

    while pila:
        nodo = pila.pop()  # toma el último elemento (LIFO)
        if nodo not in visitados:
            visitados.add(nodo)
            orden_recorrido.append(nodo)
            # Agregar vecinos en orden inverso si quieres imitar la versión recursiva
            for vecino in reversed(grafo.get(nodo, [])):
                if vecino not in visitados:
                    pila.append(vecino)

    return orden_recorrido

# Ejemplo de uso
print("Recorrido DFS (iterativo) desde A:", dfs_iterativo(grafo, "A"))
```

---

## 4. Diferencias clave entre BFS y DFS

| Característica        | BFS                                | DFS                                   |
|----------------------|-------------------------------------|---------------------------------------|
| Estructura usada     | Cola (queue)                       | Pila (stack) o recursión              |
| Estrategia           | Por niveles (anchura)              | Profundiza en un camino               |
| Camino más corto     | Sí, en grafos no ponderados        | No garantiza el más corto             |
| Uso típico           | Distancia mínima, niveles          | Existencia de camino, backtracking    |
| Consumo de memoria   | Puede ser alto en grafos anchos    | Puede ser alto en grafos muy profundos|

---

## 5. Cómo ejecutar el código en Google Colab

1. Accede a [Google Colab](https://colab.research.google.com).
2. Crea un nuevo notebook (`Archivo` → `Nuevo cuaderno`).
3. Copia y pega el código de este README en celdas separadas (por ejemplo: una celda para la definición del grafo, otra para BFS, otra para DFS).
4. Ejecuta las celdas con `Ctrl + Enter` o el botón de “play” a la izquierda.
5. Modifica el grafo y el nodo inicial para hacer tus propias pruebas.

---

## 6. Ejercicios propuestos

Puedes practicar modificando y ampliando el código:

1. **Encontrar camino específico**  
   Modifica BFS y/o DFS para que, dado un nodo `inicio` y un nodo `objetivo`, devuelva el **camino** desde `inicio` hasta `objetivo` si existe.

2. **Grafo no dirigido vs dirigido**  
   - Implementa un grafo **dirigido** (las aristas tienen dirección).
   - Observa cómo cambia el recorrido.

3. **Detección de ciclos con DFS**  
   Usa DFS para detectar si existe un ciclo en el grafo.

4. **Contar componentes conexas**  
   Aplica DFS o BFS repetidamente para contar cuántos **subgrafos conexos** hay.

---

## 7. Requisitos

Para ejecutar el código:

- **Python 3.x** (Google Colab ya lo incluye).
- Librerías estándar de Python (no se necesitan paquetes externos):
  - `collections` (para `deque` en BFS).

En un entorno local, bastaría con:

```bash
python nombre_del_script.py
```

---

## 8. Referencias básicas

- CLRS – *Introduction to Algorithms* (Cormen, Leiserson, Rivest, Stein) – Capítulos de grafos.
- Documentación de Python:  
  - [Tipos de datos — dict](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)  
  - [Módulo `collections`](https://docs.python.org/3/library/collections.html)

---

Este README pretende ser una introducción básica. Puedes ampliarlo añadiendo:
- Visualización de grafos (por ejemplo, con `networkx` y `matplotlib`).
- Variantes como BFS ponderado (Dijkstra) o DFS para ordenamiento topológico.
```
