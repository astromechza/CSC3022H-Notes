[Back](README.md)

RESOURCE ACQUISITION IS INITIALISATION
-------------------------------------------------------
- Resources created in a scope, are destroyed before the scope completes. Quite often this means a pair of opposing functions.
    - New / Delete
    - Malloc / Free
    - Aquire / Release

- The deletion is specific and often relies on the destructor function of an Automatic Variable.
```c++
class someResource
{
    //internal representation holding pointers, handles etc.

public:
    someResource()
    {
        //Obtain resource.
    }

    ~someResource()
    {
        //Release resource.
    }

};

```





[Back](README.md)