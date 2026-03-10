# BFS y DFS en un grafo

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
