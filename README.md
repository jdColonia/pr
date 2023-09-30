# **Recurrence relations and temporal complexity**
---
## **Problem 1 - Binary Search**
---
To find the recurrence relation of the binary search algorithm, we will analyze how the algorithm works:

- At each step of the binary search, the list of elements is taken and divided in half. Then it is decided whether the
  element we are looking for is in the left half or in the right half of the list, and the other half is discarded.
  Consequently, the size of the problem is reduced by half at each step. This indicates that the recurrence relation has
  the term $T\left( \frac{n}{2} \right)$
- The time it takes to compare the element we are looking for with the middle element of the list and decide which half
  of the list to keep has constant complexity.

Therefore, the recurrence relation for the binary search algorithm is $T(n) = T\left( \frac{n}{2} \right) + c.$ To solve
it and determine the complexity of the algorithm, we can use the master method. We have that $a=1$, $b=2$, $f(n)
=cn^{0}=\Theta(1)$, and therefore we have that $n^{\log_{b} a} = n^{\log_{2} 1} = n^{0}.$ We apply case 2 of the method,
since $f(n)=\Theta(1)$, so we have that the solution to recurrence is $T(n) = \Theta(\lg n).$

---
## **Problem 2 - Majority Element**
---
To find the recurrence relation for the Merge Sort algorithm, let's analyze how the algorithm works:

- At each step of Merge Sort, the list of elements is divided into two halves. Then, each half is independently sorted,
  and finally, both lists are merged. Therefore, the problem size is halved at each step, indicating that the recurrence
  relation has the term $T\left(\frac{n}{2}\right)$.
- The time it takes to merge the two lists has linear complexity since it needs to traverse all elements once.

Therefore, the recurrence relation for the Merge Sort algorithm is $T(n) = 2T\left(\frac{n}{2}\right) + cn$. To solve it
and determine the algorithm's complexity, we can use the master theorem. We have $a=2$, $b=2$, $f(n) = cn = \Theta(
n^{1})$, and therefore, we have $n^{\log_{b} a} = n^{\log_{2} 2} = n^{1}$. We apply case 2 of the master theorem since
$f(n)=\Theta(n^{1})$, so the solution to the recurrence is $T(n) = \Theta(n \log n)$.

The `isMajorityElement` function performs a linear exploration of the list once it's sorted. In the worst case, when
there is no majority element, this exploration has a time complexity of $O(n)$, where $n$ is the length of the list.

In the case where there is a majority element, the exploration will stop before completing the list, potentially making
the complexity less than $O(n)$, but in any case, it won't exceed $O(n)$.

Since sorting is the most time-consuming operation, the overall complexity of the `majorityElement` algorithm will be
dominated by the Merge Sort algorithm, which is $\Theta(n \log n)$.

---
## **Problem 3 - Organizing A Lottery**
---
To determine the recurrence relation and calculate the time complexity of the algorithm that solves the lottery problem,
we perform a detailed analysis of the different functions involved in the algorithm.

1. **Function $obtainLists(\dots)$:**
   This function takes a list of segments and splits their start and end points into two separate lists. For each
   segment, it performs a constant operation (adding the bounds to the accumulating lists) and then calls itself
   recursively on the rest of the list. Therefore, the recursion relation is defined as follows:

   $$T(n) = T(n-1) + \Theta(1)$$

   To calculate the complexity of this recurrence relation, we use the recursion tree
   method (![Recursion tree](https://i.ibb.co/6HG5vKY/Arbol-de-recursion-excalidraw.png)). At each level
   of the tree, the cost is constant, i.e., $\Theta(1)$, and there are a total of $n$ levels in the recursion.
   Therefore, the time complexity for this function is:

   $$T(n) = \Theta(n)$$

2. **Function $mergeSort(\dots)$:**
   We have previously analyzed the recurrence relation of this algorithm and found it to be as follows:

   $$T(n) = 2T(\frac{n}{2}) + cn$$

   By solving this recurrence relation, we determine in problem 2 that the time complexity of this function is:

   $$T(n) = \Theta(n \log n)$$

3. **Function $customBinarySearch(\dots)$:**
   This function implement a custom binary search. We have previously defined the recurrence equation of binary search
   as follows:

   $$T(n) = T\left(\frac{n}{2}\right) + cn$$

   And also, in the same context, we established that the solution to this recurrence relation is:

   $$T(n) = \Theta(\log n)$$

4. **Function $countSegmentsRec(\dots)$:**
   This function performs a count of the segments that include each point within a given list. For each point, the
   function counts the segments in which it is found and then invokes itself recursively to continue the analysis of the
   rest of the list. The recurrence equation is defined as:

   $$T(n) = T(n-1) + \Theta(1)$$

   To calculate the complexity of this recurrence relation, we again use the recursion tree
   method (![Recursion tree](https://i.ibb.co/6HG5vKY/Arbol-de-recursion-excalidraw.png)). At each level of the tree,
   the cost is
   $\Theta(1)$$, and there are a total of $n$ levels in the recursion. Therefore, the time complexity for this function
   is:

   $$T(n) = \Theta(n)$$

Therefore, the total complexity of the algorithm would be the sum of the complexities of these functions. However, since
we are interested in the worst-case scenario, we select the function with the highest complexity, which in this case is
$mergeSort(\dots) with a time complexity of $\Theta(n \log n)$. This means that in the worst case, the algorithm will
have a complexity of $\Theta(n \log n)$.
