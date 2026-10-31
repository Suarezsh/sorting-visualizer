# 📊 Sorting Visualizer

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Sin dependencias](https://img.shields.io/badge/Sin%20dependencias-3fb950?style=for-the-badge)
![License](https://img.shields.io/badge/Licencia-MIT-yellow?style=for-the-badge)

**Visualiza 5 algoritmos de ordenamiento animados en tiempo real.**  
Compara velocidades, conteo de operaciones y complejidad — directamente en el navegador.

**[▶ Ver demo en vivo](https://suarezsh.github.io/sorting-visualizer)**

</div>

---

## 🎯 ¿Qué es esto?

Sorting Visualizer es una herramienta educativa e interactiva para entender cómo funcionan los algoritmos de ordenamiento. Cada barra representa un elemento del arreglo y cambia de color según la operación que se está realizando.

Sin instalación, sin librerías, sin npm — solo abre `index.html`.

---

## ✨ Características

- 🎨 **Colores por estado** — cada operación tiene su propio color en tiempo real
- 📊 **5 algoritmos** — Bubble, Selection, Insertion, Merge y Quick Sort
- ⚡ **Velocidad ajustable** — desde lento (para aprender) hasta ultra rápido
- 📏 **Tamaño ajustable** — de 20 a 150 elementos
- 🧮 **Estadísticas en vivo** — comparaciones, intercambios y tiempo exacto
- 📐 **Complejidad Big-O** — muestra mejor, promedio, peor caso y espacio para cada algoritmo
- 🔄 **Generador de arreglos** — arreglo aleatorio nuevo en cualquier momento

---

## 🎨 Código de colores

| Color | Significado |
|---|---|
| 🔵 Azul | Sin ordenar (estado inicial) |
| 🟡 Amarillo | Comparando dos elementos |
| 🔴 Rojo | Intercambiando posiciones |
| 🟢 Verde | Elemento en posición final |
| 🟣 Violeta | Pivote (Quick Sort) |
| 🩵 Cian | Fusionando (Merge Sort) |

---

## 📐 Algoritmos y complejidad

| Algoritmo | Mejor caso | Caso promedio | Peor caso | Espacio |
|---|---|---|---|---|
| **Bubble Sort** | O(n) | O(n²) | O(n²) | O(1) |
| **Selection Sort** | O(n²) | O(n²) | O(n²) | O(1) |
| **Insertion Sort** | O(n) | O(n²) | O(n²) | O(1) |
| **Merge Sort** | O(n log n) | O(n log n) | O(n log n) | O(n) |
| **Quick Sort** | O(n log n) | O(n log n) | O(n²) | O(log n) |

---

## 🧠 ¿Cómo funciona cada algoritmo?

### Bubble Sort
Compara elementos adyacentes y los intercambia si están en el orden incorrecto. Repite hasta que no hay más intercambios.
```
[5, 3, 8, 1]  →  compara 5,3 → intercambia
[3, 5, 8, 1]  →  compara 5,8 → ok
[3, 5, 8, 1]  →  compara 8,1 → intercambia
[3, 5, 1, 8]  →  8 está en su lugar ✓
```

### Selection Sort
Busca el elemento mínimo del subarreglo sin ordenar y lo coloca al inicio.
```
[5, 3, 8, 1]  →  mínimo = 1 → intercambia con posición 0
[1, 3, 8, 5]  →  mínimo = 3 → ya está en posición 1
[1, 3, 8, 5]  →  mínimo = 5 → intercambia con posición 2
[1, 3, 5, 8]  →  ordenado ✓
```

### Insertion Sort
Toma cada elemento y lo inserta en la posición correcta del subarreglo ya ordenado.
```
[5, 3, 8, 1]  →  toma 3, lo inserta antes del 5
[3, 5, 8, 1]  →  toma 8, ya está bien
[3, 5, 8, 1]  →  toma 1, lo inserta al inicio
[1, 3, 5, 8]  →  ordenado ✓
```

### Merge Sort
Divide el arreglo a la mitad recursivamente, luego fusiona las mitades ordenadas.
```
[5, 3, 8, 1]
   ↙      ↘
[5, 3]   [8, 1]
 ↙  ↘    ↙  ↘
[5][3]  [8] [1]
 ↘  ↙    ↘  ↙
[3, 5]  [1, 8]
    ↘   ↙
 [1, 3, 5, 8] ✓
```

### Quick Sort
Elige un pivote, coloca menores a la izquierda y mayores a la derecha, repite recursivamente.
```
[5, 3, 8, 1]  →  pivote = 1
[1 | 3, 5, 8]  →  pivote = 5
[1, 3 | 5 | 8]  →  ordenado ✓
```

---

## 🖥️ Vista previa

```
┌─────────────────────────────────────────────────────────────┐
│  📊 Sorting Visualizer                    5 algoritmos · RT │
├─────────────────────────────────────────────────────────────┤
│  [Bubble] [Selection] [Insertion] [Merge] [Quick]           │
│  Mejor: O(n)  Promedio: O(n²)  Peor: O(n²)  Espacio: O(1) │
├─────────────────────────────────────────────────────────────┤
│  ▁▂▃▇▄▅▆█▂▃▄▅▇▆▁▂▃▇▄▅▆█▂▃▄▅▇▆▁▂▃▇▄▅▆   [Ordenando…]      │
│  ▁▂▃▇▄▅▆█▂▃▄▅▇▆▁▂▃▇▄▅▆█▂▃▄▅▇▆▁▂▃▇▄▅▆                      │
├───────────┬──────────┬─────────────┬──────────────────────-─┤
│  Compar.  │ Interc.  │ Tiempo (ms) │ Elementos              │
│   2,841   │   643    │    142      │    60                  │
├─────────────────────────────────────────────────────────────┤
│  [▶ Iniciar] [⟳ Nuevo]  Tamaño ──●──  Velocidad ──●──      │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 Uso

```bash
git clone https://github.com/Suarezsh/sorting-visualizer.git
cd sorting-visualizer

# Opción 1: abrir directo
start index.html        # Windows
open  index.html        # macOS

# Opción 2: servidor local
python -m http.server 8080
```

---

## 📁 Estructura

```
sorting-visualizer/
└── index.html    ← Todo en un solo archivo (HTML + CSS + JS)
```

---

## 🛠️ Tecnologías

- **HTML5 Canvas** — renderizado de las barras con efectos de brillo
- **JavaScript ES6+** — algoritmos con `async/await` para animación fluida
- **CSS Grid / Flexbox** — layout responsive
- **Google Fonts** — Space Grotesk + JetBrains Mono
- **Sin frameworks · Sin librerías · Sin npm**

---

## 🗺️ Próximas mejoras

- [ ] Heap Sort y Shell Sort
- [ ] Modo de comparación side-by-side entre dos algoritmos
- [ ] Sonido sincronizado con las operaciones
- [ ] Exportar la animación como GIF
- [ ] Modo de arreglo casi ordenado vs. invertido

---

## 📄 Licencia

MIT © [Suarezsh](https://github.com/Suarezsh)
