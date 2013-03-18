[Back](README.md)

REFERENCES
-------------------------------------------------------
C++ pointers are very powerful but unsafe. The alternative to pointers are REFERENCES!
- Syntax:
    ```c++
    someobject O;
    someobject & oref = O;
    ```
    Modifications to oref modify O.

- Pointers vs References
    * Pointers
        ```c++
        int i = 5;
        int * iptr = &i;
        cout << *iptr << endl;      //5
        *iptr = 6;                  //set 6
        cout << i << endl;          //6

        ```
    * References
        ```c++
        int i = 5;
        int & iref = i;
        cout << iref << endl;       //5
        iref = 6;                   //set 6
        cout << i << endl;          //6

        ```




[Back](README.md)