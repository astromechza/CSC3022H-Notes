[Back](README.md)

THE 4 SPECIAL MEMBER FUNCTIONS
-------------------------------------------------------

## DEFAULT CONSTRUCTOR
```c++
someclass(int a)
{
    somevariable = a;
}
```

## COPY CONSTRUCTOR
```c++
someclass(const someclass& other)
{
    somevariable = other.somevariable;
}
```

## COPY ASSIGNMENT OPERATOR
```c++
someclass & operator=(const someclass & other)
{
    if(this != &other)
    {
        somevariable = other.somevariable;
    }
    return *this;
}
```

## DESTRUCTOR
```c++
~someclass()
{
    delete somepointer;
}
```

[Back](README.md)