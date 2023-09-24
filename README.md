# **Organizing a lottery**

#### **Proof of Algorithm Correctness:**

#### **Recurrence relation and algorithmic complexity:**

To determine the recurrence relation and calculate the time complexity of the algorithm that solves the lottery
problem, we conduct a detailed analysis of the various functions involved in the algorithm:

1. **Function $obtainLists(\dots)$:**
   This function takes a list of segments and divides each segment into two parts, adding them to two accumulating
   lists. For each segment, it performs a constant-time operation (adding boundaries to the accumulating lists) and then
   calls itself recursively on the rest of the list. Therefore, the recurrence relation is defined as follows:

   $$T(n) = T(n-1) + \Theta(1)$$

   To calculate the complexity of this recurrence relation, we use the recursion tree
   method (![Árbol de recursión](https://i.ibb.co/VYdMbR6/Arbol-de-recursion-obtain-List-excalidraw.png)). At each level
   of the tree, the cost is constant, i.e., $\Theta(1)$, and there are a total of $n$ levels in the recursion.
   Therefore, the time complexity for this function is:

   $$T(n) = \Theta(n)$$

2. **Function $mergeSort(\dots)$:**
   We have previously analyzed the recurrence relation of this algorithm and found it to be as follows:

   $$T(n) = T(n-1) + \Theta(1)$$

   By solving this recurrence relation, we determined that the time complexity of this function is:

   $$T(n) = \Theta(n \log n)$$

3. **Functions $customBinarySearch(\dots)$:**
   This function implement a custom binary search. We have previously defined the recurrence equation of binary search
   as follows:

   $$T(n) = T\left(\frac{n}{2}\right) + cn$$

   And also, in the same context, we established that the solution to this recurrence relation is:

   $$T(n) = \Theta(\log n)$$

4. **Function $countSegmentsRec(\dots)$:**
   This function counts the segments that contain each point in a list of points. For each point, it performs a binary
   search on the lists of segment starts and ends (which takes logarithmic time in the number of segments), and then
   calls itself recursively on the rest of the list. The recurrence equation is defined as follows:

   $$T(n) = T(n-1) + \Theta(\log n)$$

   To calculate the complexity of this recurrence relation, we again use the recursion tree
   method (![Árbol de recursión](https://i.ibb.co/kmHjVYk/Arbol-de-recursion-count-Segments-Rec-excalidraw.png)). At
   each level of the tree, the cost is $\log n - i$, where $i$ is the current level, and there are a total of $n$ levels
   in the recursion.Therefore, the time complexity for this function is:

   $$T(n) = \Theta(n \log n)$$

Therefore, the total complexity of the algorithm would be the sum of the complexities of these functions. However, since
we are interested in the worst-case scenario, we select the function with the highest complexity, which in this case is
$mergeSort(\dots)$ and $countSegmentsRec(\dots)$, both with a time complexity of $\Theta(n \log n)$. This means that in
the worst case, the algorithm will have a complexity of $\Theta(n \log n)$.
