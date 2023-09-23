# **Organizing a lottery**

#### **Recurrence relation and algorithmic complexity:**

Para encontrar la relación de recurrencia del algoritmo que resuelve el problema de la lotería, analizaremos el bloque
de código que resuelve el problema:

- $obtainLists(...)$: Esta función toma una lista de segmentos y divide cada segmento en dos partes, agregándolas a dos
  listas acumuladoras. Para cada segmento, realiza una operación constante (agregar los límites a las listas
  acumuladoras)
  y luego se llama a sí misma recursivamente en el resto de la lista. Por lo tanto, la relación de recurrencia es
  $$T(n) = T(n-1) + \Theta(1)$$
  Para calcular la complejidad de esa relación de recurrencia usamos el método de árboles de recursión:
  ![Árbol de recursión](https://i.ibb.co/VYdMbR6/Arbol-de-recursion-obtain-List-excalidraw.png)
  Como podemos notar, en cada nivel del árbol, el costo es $1$, y hay $n$ niveles en total. Por lo tanto, la complejidad
  de tiempo es: $$T(n) = \Theta(n)$$
- $mergeSort(...)$: Como hemos analizado en el problema 2, la relación de recurrencia de este algoritmo es
  $$T(n) = 2T\left(\frac{n}{2}\right) + \Theta(n)$$
  y al solucionar esta relación de recurrencia, nos dio que la complejidad es
  $$T(n) = \Theta(n \log n)$$
- $customBinarySearch1(...)$ y $customBinarySearch2(...)$: Estas funciones implementan una búsqueda binaria
  personalizada
  y, como sabemos, en el problema 1 definimos que la ecuación de recurrencia de la búsqueda binaria es
  $$T(n) = T\left(\frac{n}{2}\right) + \Theta(1)$$
  y también en ese mismo problema dijimos que la solución de esa relación de recurrencia es
  $$T(n) = \Theta(\log n)$$
- $countSegmentsRec(...)$: Esta función cuenta los segmentos que contienen cada punto en una lista de puntos.
  Para cada punto, realiza una búsqueda binaria en las listas de inicio y fin de los segmentos (que toma tiempo
  logarítmico
  en el número de segmentos), y luego se llama a sí misma recursivamente en el resto de la lista. Por lo tanto, la
  ecuación
  de recurrencia es
  $$T(n) = T(n-1) + \Theta (\log n)$$
  Para calcular la complejidad de esa relación de recurrencia usamos el método de árboles de recursión:
  ![Árbol de recursión](https://i.ibb.co/kmHjVYk/Arbol-de-recursion-count-Segments-Rec-excalidraw.png)
  Como podemos notar, en cada nivel del árbol, el costo es $\log n - i$, y hay $n$ niveles en total. Por lo tanto, la
  complejidad de tiempo es:
  $$T(n) = \Theta(n \log n)$$
  Por lo tanto, la complejidad total del algoritmo sería la suma de las complejidades de estas funciones. Sin embargo,
  como estamos interesados en el peor caso, tomamos la función con la mayor complejidad. En este caso, eso son
  $mergeSort(...)$
  y $countSegmentsRec(...)$ con una complejidad de tiempo de $\Theta(n \log n)$. Esto significa que en el peor caso,
  el algoritmo tendrá una complejidad temporal de $\Theta(n \log n)$.
