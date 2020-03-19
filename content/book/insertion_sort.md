+++
title = "Insertion Sort"
author = ["Hans Pistor"]
date = 2020-03-18T00:00:00-04:00
draft = false
+++

>Input: **A sequence of n numbers {a<sub>1</sub>, a<sub>2</sub>, a<sub>3</sub>, ... a<sub>n</sub>}**

>Output: **a permutation of {a<sub>1</sub>, a<sub>2</sub>, a<sub>3</sub>, ... a<sub>n</sub>} such that a<sub>1</sub>' < a<sub>2</sub>' < a<sub>n</sub>'**


## How it works {#how-it-works}

Basically the way most people sort a hand of playing cards. We start with an
empty left hand and the the card face down. We remove one card at a time and
insert it into the correct position of the hand. To find the right spot, we
compare it to the card already in the hand from right to left.

_Sorts in place_

```python
def insertion_sort(arr):
    print("Unsorted arr: " + str(arr))
    for j in range(1, len(arr)):
        key = arr[j]
        i = j-1
        while i >= 0 and arr[i] > key:
            arr[i+1] = arr[i]
            i = i-1
        arr[i+1] = key
    print("Sorted arr: " + str(arr))

insertion_sort([5, 2, 4, 6, 1, 3])
```

```text
Unsorted arr: [5, 2, 4, 6, 1, 3]
Sorted arr: [1, 2, 3, 4, 5, 6]
```
