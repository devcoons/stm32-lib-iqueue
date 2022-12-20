# IQUEUE LIBRARY
[![C/C++ CI](https://github.com/devcoons/stm32-lib-iqueue/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/devcoons/stm32-lib-iqueue/actions/workflows/build.yml)  [![Codacy Badge](https://app.codacy.com/project/badge/Grade/917370c0758748ac8fa5c1c56e58d5cc)](https://www.codacy.com/gh/devcoons/stm32-lib-iqueue/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=devcoons/stm32-lib-iqueue&amp;utm_campaign=Badge_Grade)

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
typedef struct 
{
   uint8_t a[8];
   uint8_t b[8];
}data_t;

...
...

uint8_t storage[256];
iqueue_t queue;	

...
...

iqueue_init(&queue, 16,	sizeof(data_t), storage);

...
...

data_t d;
iqueue_enqueue(&queue,&d);

...
...

data_t r;
iqueue_dequeue(&queue,&r);

```
