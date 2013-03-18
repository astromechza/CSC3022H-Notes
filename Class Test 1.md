C++ TEST 1 NOTES - MARCH 2013
=============================



SCOPE : section of code a variable is visible
---------------------------------------------
- In C++, generally between { }
- { } can be nested:
    ```c++
    for (int a = 0; a < 5; ++a)
    {
        for (int b = 0; b < 5; ++b)
        {

        }
    }
    ```
        
- Inner vars override outer vars and changes to inner don't affect outer.
    ```c++
    int i = 0;
    for (int j = 0; j< 5; ++j)
    {
        int i = 1;
        assert (i == 1)     //true
    }
    ```

- File/global scope exists outside of function { }'s
    ```c++
    int one = 1;
    void whatisone()
    {
        int one = 2;        
        assert (one == 2)   //true
    }
    ```

- Scope resolution can be used to access a variable in global ( ::var ) or namespace ( namespace::var )


NAMESPACES : a scope construct
------------------------------
- Used to stop duplication 
    ```c++
    namespace john
    {
        int hello = 100;
    }

    namespace bob
    {
        int hello = 200;
    }
    ```

- Explicit access
    ```c++
    john::hello
    ```

- Explicit 'using'
    ```c++
    using john::hello;
    assert ( hello = 100 )
    ```

- General 'using'   
    ```c++
    using john;
    assert ( hello = 100 )
    ```

- Namespaces can extend each other
    ```c++
    namespace carl
    {
        int i = 0;
    }

    namespace carl
    {
        void checki()
        {
            assert (i == 0)
        }
    }
    ```

- Namespaces can be aliased
    ```c++
    namespace wtfthisnamespaceistoolong
    {
        int something = 2;
    }

    namespace tiny = wtfthisnamespaceistoolong;
    ```


POINTERS
--------
