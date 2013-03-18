HEADER FILES : hold declarations for other files to use
-------------------------------------------------------

## FORWARD DECLARAIONS
```.cpp``` files can ```#include``` header files in order to gain forward knowledge of 
members. Including a header file (which contains other includes and forward declarations). 
```c++
// in the header:
int add(int x, int y);

// in the cpp:
int add(int x, int y)
{
    return x+y;
}
```

## HEADER GUARD
The compiler will complain if we declare things multiple times and overwrite them. So we use preprocessor
directives to stop the compiler from including a header file multiple times in a single file:

```c++
#ifndef _SOME_UNIQUE_NAME_
#define _SOME_UNIQUE_NAME_

// do definitions here

#endif
```

## INCLUDES IN OTHER FILES
