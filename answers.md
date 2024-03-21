# CMPS 2200 Reciation 5
## Answers

**Name:**_________Frankie Soltero________________


Place all written answers from `recitation-05.md` here for easier grading.







- **1b.**

For Quick sort fixed and random the asymptotic bound is O(nlogn) on average case. The run times are pretty normal and increase as the list size increases

For selection sort, the asymptotic upper bound is n^2 for all cases. The run times match

Quick sort tends to lean towards being quicker on random permutation compared to random ones, the difference is esepcially noticable at larger inputs as we saw using the test pring function. For selection sort it remains pretty consistent but at larger inputs it will be much slower as it needs to iterate through the whole list. Overall quick sort is much more effected by the types of lists given v selection sort that remains pretty constant


- **1c.**
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
