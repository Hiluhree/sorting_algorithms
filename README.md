# 0x1B. C - Sorting algorithms & Big O
### Resources
+ [Sorting algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm)
+ [Big O notation](https://stackoverflow.com/questions/487258/what-is-a-plain-english-explanation-of-big-o-notation)
+ [Sorting algorithms animations](https://www.toptal.com/developers/sorting-algorithms)
+ [15 sorting algorithms in 6 minutes](https://www.youtube.com/watch?v=kPRA0W1kECg) (**WARNING**: The following video can trigger seizure/epilepsy. It is not required for the project, as it is only a funny visualization of different sorting algorithms)
+ [CS50 Algorithms explanation in detail by David Malan](https://www.youtube.com/watch?v=yb0PY3LX2x8&t=2s)
+ [All about sorting algorithms](https://www.geeksforgeeks.org/sorting-algorithms/)

#### Data Structure and Functions
For this project you are given the following print_array, and print_list functions:
```
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
```
```
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
```

Our files``print_array.c`` and ``print_list.c`` (containing the ``print_array`` and ``print_list`` functions) will be compiled with your functions during the correction.
Please declare the prototype of the functions ``print_array`` and ``print_list`` in your ``sort.h`` header file
Please use the following data structure for doubly linked list:
```
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```

Please, note this format is used for Quiz and Task questions.
+ ``O(1)``
+ ``O(n)``
+ ``O(n!)``
+ n square -> ``O(n^2)``
+ log(n) -> ``O(log(n))``
+ n * log(n) -> ``O(nlog(n))``
+ n + k -> ``O(n+k)``
+ …
Please use the “short” notation (don’t use constants). Example: ``O(nk)`` or ``O(wn)`` should be written ``O(n)``. If an answer is required within a file, all your answers files must have a newline at the end.

Tests
Here is a quick tip to help you test your sorting algorithms with big sets of random integers: [Random.org](https://www.random.org/integer-sets/)
