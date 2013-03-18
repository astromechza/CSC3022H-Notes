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
float thismeansthesamething = **pointertoapointer; 
```

## & REFERENCE
- When given an object, you can get a pointer to it by using this reference operator ```&```
```c++

float actualvalue = 3.1415f;
float *pointer = &actualvalue;

//the pointer can be then be used to change the actualvalue:
*pointer = 100f;
```

## POINTER MODIFICATION
- A pointer just contains a memory address. Since this is a number, it can be modified just as any other numerical type
could.
```c++
float actualvalue = 3.1415f;
float *pointer = &actualvalue;
pointer+=1;                         // the pointer now points 1 sizeof(float) forward.
```

- BUT. Although you can set the pointer address to whatever you want, you might not be able to read or write the values at
that position. This is to ensure that other programs don't access memory they shouldn't be allowed to access. This is often 
what causes a *SEGFAULT*.

## GENERIC POINTERS
- ```void * something;``` indicates a pointer that can point to any type of object.
- These are useful for generic functions.
- Generic pointers must be 'cast' in order to use the returned value, since we have no idea what the structure of the memory 
region is without knowing what object is represented.

## POINTER & ARRAYS
- In C++ an array object actually is a pointer to the first element in the array.
- The squarebracket notation when denoting an array size just reserves the block of memory for N objects.
- 2D arrays are also stored in a continuous region, the sub elements are not pointers to arrays, they are arrays themselves.
- Access the N'th element using pointer arithmetic:
```c++
int numbers[10];

numbers[0] = 88;
numbers[1] = 99;

int * ptr = &numbers[0];
std::cout << *ptr << std::endl;         // 88 
std::cout << *(ptr+1) << std::endl;     // 99
```

```c++
char stuff[] = "bob";
std::cout << stuff[0] << std::endl;
std::cout << stuff[1] << std::endl;
std::cout << stuff[2] << std::endl;

char* stuff2 = "ann";
std::cout << *(stuff2+0) << std::endl;
std::cout << *(stuff2+1) << std::endl;
std::cout << *(stuff2+2) << std::endl;

// get the char * to the first character
char* stuff3 = stuff;
std::cout << *(stuff3+0) << std::endl;
std::cout << *(stuff3+1) << std::endl;
std::cout << *(stuff3+2) << std::endl;
```


[Back](README.md)