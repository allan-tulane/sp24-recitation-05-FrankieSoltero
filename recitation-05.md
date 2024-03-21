# CMPS 2200 Recitation 5

In this recitation, we'll look at randomness in computation.

**To make grading easier, please place all written solutions directly in `answers.md`, rather than scanning in handwritten work or editing this file.**

All coding portions should go in `main.py` as usual.


## Determinism versus Randomization in Quicksort

In lecture we saw that adding a random choice of pivot reduced the
probability of worst-case behavior for any given input in
selection. Let's look at how pivot choices affect Quicksort. For this
question, refer to the code in `main.py` 

**1a)**

Complete the implementations of `qsort` and `compare_sort` stubs. Feel
free to take from code given in the lectures to  help you perform list
partitioning. Note that the pivot choice function is input to `qsort`,
so you will have to curry `qsort` to test different methods of
choosing pivots. Implement variants of `qsort` that correspond to
selecting the first element of the input list as the pivot, and to
selecting a random pivot.
.  
.  
.  
.  


**1b)**

Compare running times using `compare-sort` between variants of
Quicksort and the
provided implementation of selection sort (`ssort`). Perform two
different comparisons: a comparison between sorting methods using
random permutations of the specified sizes, and a comparison using
already sorted permutations. How do the running times compare to the
asymptotic bounds? How does changing the type of input list change the
relative performance of these algorithms? Note that you may have to
modify the list sizes based on your system memory; compare at least 10
different list sizes. The `print_results` function in `main.py` gives
a table of results, but feel free to use code from Lab 1 to plot
the results as well. 

For Quick sort fixed and random the asymptotic bound is O(nlogn) on average case. The run times are pretty normal and increase as the list size increases

For selection sort, the asymptotic upper bound is n^2 for all cases. The run times match

Quick sort tends to lean towards being quicker on random permutation compared to random ones, the difference is esepcially noticable at larger inputs as we saw using the test pring function. For selection sort it remains pretty consistent but at larger inputs it will be much slower as it needs to iterate through the whole list. Overall quick sort is much more effected by the types of lists given v selection sort that remains pretty constant



**1c)**

Python uses a sorting algorithm called [*Timsort*](https://en.wikipedia.org/wiki/Timsort), designed by Tim Peters. Compare the fastest of your sorting implementations to the Python
sorting function `sorted`, conducting the tests in 1b above. 
As seen below the qsort random pivot is the fastest 

|        |         |       n |   timsort           |   qsort-random-pivot |
|--------|---------|---------|---------------------|----------------------|
|    100 |   0.218 |   0.276 |               0.009 |                0.005 |
|    200 |   0.430 |   0.492 |               0.015 |                0.011 |
|    500 |   1.049 |   1.225 |               0.055 |                0.036 |
|   1000 |   2.327 |   2.590 |               0.084 |                0.076 |
|   2000 |   4.205 |   4.870 |               0.164 |                0.159 |
|   5000 |  11.227 |  12.522 |               0.440 |                0.429 |
|  10000 |  23.155 |  25.002 |               0.967 |                0.927 |
|  20000 |  49.019 |  53.122 |               2.081 |                2.020 |
|  50000 | 127.537 | 140.184 |               5.867 |                5.780 |
| 100000 | 273.341 | 311.143 |              12.497 |               12.437 |

