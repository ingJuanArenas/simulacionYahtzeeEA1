# 🎲 Simulación Yahtzee — Montecarlo

**Evaluación de Actividad 1 · Simulación · PREICA2601B020049**  
![Python](https://img.shields.io/badge/Python-3.8+-blue) ![Colab](https://img.shields.io/badge/Google-Colab-orange) ![Método](https://img.shields.io/badge/Método-Montecarlo-green)

---

## Descripción

Simulación del juego Yahtzee para 2 jugadores usando el método de Montecarlo para tomar decisiones óptimas en cada turno. El programa evalúa las 32 combinaciones posibles de dados a guardar y selecciona la que maximiza el valor esperado de puntuación, calculado mediante 300 simulaciones por decisión.

---

## Estructura del repositorio

```
simulacionYahtzeeEA1/
├── SimulaciónEA1Yahtzee.ipynb     # Notebook principal (Google Colab)
├── README.md

```

---

## Cómo ejecutar

**En Google Colab (recomendado):**

1. Ir a [colab.research.google.com](https://colab.research.google.com)
2. Archivo → Abrir cuaderno → GitHub
3. Pegar la URL de este repositorio
4. Ejecutar todas las celdas: `Entorno de ejecución → Ejecutar todo`

**Localmente:**

```bash
git clone https://github.com/ingJuanArenas/simulacionYahtzeeEA1.git
cd simulacionYahtzeeEA1
pip install matplotlib
jupyter notebook SimulaciónEA1Yahtzee.ipynb
```

---

## Método de Montecarlo aplicado

La función `elegir_mascara_bloqueo_montecarlo()` determina qué dados guardar en cada momento del turno:

1. Genera las **32 máscaras binarias** posibles (2⁵ combinaciones de 5 dados)
2. Para cada máscara, simula **300 tiradas futuras** del turno
3. Calcula el **valor esperado promedio** de puntuación por combinación
4. Elige la máscara con el mayor puntaje esperado

---

## Resultados (semilla 42)

```
Jugador 1: 91 pts   |   Jugador 2: 135 pts   →   Ganador: Jugador 2

Total lanzamientos individuales: 390
Distribución observada por cara: 13.1% – 18.7%
Probabilidad teórica esperada:   16.67% (uniforme)
```

La distribución observada confirma que el generador de números aleatorios de Python se comporta como un dado justo, con desviaciones mínimas respecto al valor teórico (Ley de los Grandes Números).

---



