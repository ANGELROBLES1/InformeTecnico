# Informe Técnico del Proyecto: Gestor Inteligente de Estructuras de Datos Lineales

## 1. Introducción
![image](https://github.com/user-attachments/assets/5f690449-d434-4f9c-a1d5-7304928a6a55)

El presente informe documenta el desarrollo e implementación de una aplicación educativa e interactiva denominada **"Gestor Inteligente de Estructuras de Datos Lineales"**, cuyo objetivo principal es facilitar la visualización, operación y análisis de rendimiento de diversas estructuras de datos lineales. El sistema fue desarrollado en **Python** utilizando **Tkinter** para la interfaz gráfica, y está orientado a estudiantes y profesionales que deseen comprender el funcionamiento interno, la eficiencia y el uso práctico de estas estructuras en escenarios reales.

El gestor permite seleccionar entre listas simples, listas dobles, pilas y colas; ejecutar operaciones básicas como inserción, eliminación, búsqueda, recorrido y obtener el tamaño. Además, incluye una funcionalidad de **benchmarking** que analiza el desempeño temporal y el uso de memoria en función del número de elementos gestionados.

---

## 2. Diseño e Implementación de las Estructuras
![image](https://github.com/user-attachments/assets/b83fac7d-df6f-4627-bc57-25f0b9829731)

Cada estructura fue implementada desde cero en Python siguiendo paradigmas orientados a objetos. A continuación, se describen sus características:

### 2.1 Lista Simple
- Implementada con nodos enlazados hacia adelante.
- Operaciones: insertar al inicio y final, eliminar al inicio y final, buscar, recorrer y tamaño.
- Ideal para inserciones rápidas al inicio y recorridos unidireccionales.

### 2.2 Lista Doble
- Cada nodo tiene referencias hacia adelante y atrás.
- Operaciones similares a la lista simple, pero se incluye recorrido en reversa.
- Útil cuando se necesita recorrer en ambas direcciones o eliminar nodos desde ambos extremos con eficiencia.

### 2.3 Pila (implementada con lista enlazada)
- Comportamiento LIFO (Last-In, First-Out).
- Operaciones: apilar, desapilar, ver tope y tamaño.
- Útil en algoritmos como retroceso (backtracking) o ejecución de expresiones.

### 2.4 Cola Simple
- Comportamiento FIFO (First-In, First-Out).
- Operaciones: encolar, desencolar, ver frente y tamaño.
- Útil en sistemas de procesamiento por turnos y buffers.

---

## 3. Benchmark: Resultados y Análisis
![image](https://github.com/user-attachments/assets/632a5c2a-97a1-445d-9cdc-db627c6c3c7c)

Se ejecutaron pruebas de rendimiento temporal y de consumo de memoria usando la biblioteca `tracemalloc` y `time`.

### 3.1 Resultados por estructura
  3  Pruebas por Estructura

| Estructura     | Tiempo (s) | Memoria (KB) |
|----------------|------------|---------------|
| Lista Simple   | 0.000198   | 11.18         |
| Lista Simple   | 0.008915   | 109.60        |
| Lista Simple   | 0.166534   | 578.34        |
| Lista Doble    | 0.000249   | 13.57         |
| Lista Doble    | 0.010871   | 120.24        |
| Lista Doble    | 0.199272   | 612.89        |
| Pila           | 0.000138   | 10.24         |
| Pila           | 0.007103   | 101.93        |
| Pila           | 0.143237   | 544.76        |
| Cola           | 0.000179   | 11.09         |
| Cola           | 0.008274   | 108.74        |
| Cola           | 0.160835   | 568.32        |

---

## 4. Análisis y Observaciones

### 4.1 Análisis Comparativo

- Las estructuras más eficientes en tiempo y memoria fueron la **Pila** y la **Cola**, debido a la sencillez de sus operaciones LIFO y FIFO.
- La **Lista Doble** presenta el mayor consumo de memoria por mantener dos referencias en cada nodo.
- La **Lista Simple** se posiciona como una estructura intermedia en términos de consumo y tiempo.

### 4.2 Promedios Generales

| Estructura     | Tiempo Promedio (s) | Memoria Promedio (KB) |
|----------------|---------------------|-------------------------|
| Lista Simple   | 0.058549            | 233.04                  |
| Lista Doble    | 0.070131            | 248.90                  |
| Pila           | 0.050159            | 218.31                  |
| Cola           | 0.056429            | 229.38                  |

---

## 5. Observaciones y Casos de Uso

- Las estructuras fueron reiniciadas al ser seleccionadas para evitar datos residuales.
- El benchmark es reproducible y se basa en las operaciones ejecutadas por el usuario en la interfaz.
- Las **listas dobles** son útiles cuando se necesita recorrer o modificar la estructura desde ambos extremos.
- Las **pilas** y **colas** se ajustan bien a contextos como navegadores web (historial), editores de texto (undo) o impresoras (spooling).

---

## 6. Mejoras a Futuro

- Incluir estructuras no lineales como árboles y grafos.
- Agregar animaciones para visualizar los cambios en tiempo real.
- Exportar reportes automáticos en PDF de las operaciones y benchmarks.
- Implementar pruebas de rendimiento con hilos (concurrente).
- Soporte para importar datos desde archivos CSV o Excel.

---

## 7. Conclusiones

El desarrollo del **Gestor Inteligente de Estructuras Lineales** permite no solo operar con estructuras fundamentales en informática, sino también observar su desempeño en condiciones controladas. La incorporación del benchmarking es clave para entender el comportamiento algorítmico más allá del código fuente, lo que permite decisiones informadas en el diseño de soluciones eficientes.

El sistema demuestra que:
- Cada estructura tiene ventajas dependiendo del contexto de uso.
- Las diferencias de tiempo y memoria son notorias a medida que crece la carga.
- El diseño modular y la visualización de operaciones facilitan el aprendizaje y la evaluación de algoritmos.

Este proyecto puede extenderse a nuevos dominios educativos o profesionales, integrando visualización avanzada y análisis profundo para estructuras más complejas.
