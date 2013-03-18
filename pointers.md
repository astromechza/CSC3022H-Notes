[Back](README.md)

POINTERS!! (yay what fun)
-------------------------------------------------------
- A pointer is the address of a thing in memory.
- A pointer variable is a variable which stores such an address. ```Object *pointerv;```
- Takes up 32 bit on a 32bit system, 64 bit on a 64bit system. Because it must cover the entire RAM.

## * DEREFERENCE
- When given a pointer, one can resolve it to the actual object it represents by using the ```*``` operator.
```c++
float *ptr;     // some pointer to some float
float actualvalue = *ptr;
```

- Of course in some cases multiple levels of pointers may have been used:
```c++
float **pointertoapointer;
float *pointer = *pointertoapointer;
float actualvalue = *pointer;

float thismeansthesamething = **pointertoapointer; ```

## & REFERENCE





[Back](README.md)