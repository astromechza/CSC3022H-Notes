[Back](README.md)

OPERATOR OVERLOADING
-------------------------------------------------------
You can implement C++ operator overloads by providing special member-functions on your classes that follow a particular naming convention.

- The following operators can be overloaded in user-defined classes:
```
+    -    *    /    =    <    >    +=   -=   *=   /=   <<   >>
<<=  >>=  ==   !=   <=   >=   ++   --   %    &    ^    !    |
~    &=   ^=   |=   &&   ||   %=   []   ()   ,    ->*  ->   new 
delete    new[]     delete[]
```

- A simple example:
    ```c++
    MyClass & MyClass::operator=(const MyClass &rhs)
    {
        if (this != &rhs) 
        {
          // Deallocate, allocate new space, copy values...
        }

        return *this;
      }
    ```

- Most simple operators return a reference to the 'after' object and take an argument, the 'before' object.
    ```c++
     MyClass & MyClass::operator+=(const MyClass &rhs)
     {
        // Do the compound assignment work.

        return *this;
      }
    ```

- PLUS
    ```c++
      const MyClass MyClass::operator+(const MyClass &other) const 
      {
        return MyClass(*this) += other;
      }

    ```

- EQUAL
    Return a boolean, take in an 'other'
    ```c++
    bool MyClass::operator==(const MyClass &other) const
    {
        // Compare the values, and return a bool result.
    }

    ```

- NOT EQUAL
    use the ==
    ```c++
    bool MyClass::operator!=(const MyClass &other) const 
    {
        return !(*this == other);
    }
    ```




[Back](README.md)