# IQUEUE LIBRARY
![C/C++ CI](https://github.com/devcoons/stm32-lib-iqueue/workflows/C/C++%20CI/badge.svg)  [![Codacy Badge](https://app.codacy.com/project/badge/Grade/917370c0758748ac8fa5c1c56e58d5cc)](https://www.codacy.com/gh/devcoons/stm32-lib-iqueue/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=devcoons/stm32-lib-iqueue&amp;utm_campaign=Badge_Grade)

*Compiler flags: **-O3 -Wfatal-errors -Wall -std=c11***

Library for creating and manage queues.


## Functions Guide

- `iqueue_init`: initializes the structure.
- `iqueue_enqueue`: puts an element at the end of the queue.
- `iqueue_dequque`: takes out the first element of the queue.
- `iqueue_size`: gets the size of the queue (number of elements).
- `iqueue_advance_next`: advances a position in the queue.
- `iqueue_get_next_enqueue`: returns the next element of the queue.
- `iqueue_dequeue_fast`: returns the first element of the queue.


## How to use

- Include the header file `lib_iqueue.h`.
- Create a `iqueue_t` instance.
- Initialize the queue using `iqueue_init`
   

## Example

```C


```