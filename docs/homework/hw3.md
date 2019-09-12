---
layout: page
title: Homework 3
subtitle: BCB-5300 Algorithms in Computational Biology (Fall 2019)
---

### Homework 3 Solution

Let P = TACTA and T = TACTAGTACTACTA. 

1. (2 points) Preprocess P in preparation to implementing the KMP algorithm. Construct a table like the lecture slides containing P, q, and pm[q].

2. (3 points) Solve the Exact Matching problem for (P, T) using the KMP algorithm. Give a table that documents your execution of KMP. The first column should contain i (pointer to the text). The second column should contain q (points to the most matches in the pattern). The third column should contain pm[q]. The fourth (last) column is the comment that should contain what happened in the corresponding line. Each row should represent a match found, a mismatch found, pattern found, a terminate, or any action based on changing of i and q. 

3. (5 points) Implement the KMP algorithm based on the pseudocode of the lecture slide. Then send me an email your jupyter notebook containing your code and output of above example.

4. (+2 points) The first algorithms is from the lecture slides. Try to Re-implement the KMP algorithm as bottom skeleton to work with for loop, not while loop.

```
def KMP(pattern, text):
    n = len(pattern)
    m = len(text)
    occurrences = []
    pm = PartialMatchTableAdvanced(pattern)
    q = 0  # q points to the most matches in the pattern so far
    i = 0  # i is the pointer to the text where the pattern is currently aligned to
    while (i < m):

    ....

    return occurrences;
```

to

```
def KMP2(pattern, text):
    n = len(pattern)
    m = len(text)
    occurrences = []
    pm = PartialMatchTableAdvanced(pattern)
    q = 0
    for i in range (0, m):

    ....

    return occurrences;
```
