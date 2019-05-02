# Notes for C++ syntax and C++17
Using this note to track down the missing knowledge for C++ in the following aspects
1. Basic C++ syntax recap
2. C++17 special syntax and extension
3. OOP related special details
## C++ general syntaxes
* C-style array
```cpp
int myArray[3] = {0} // Initialize myArray with all zeros
int myArray[3] = {} // Same as above, don't need 0
int myArray[] = {1,2,3,4} // Initialize with 4 elements
// If C++17 compiler, we can use the following to get size
unsigned int arraySize = std::size(myArray);
```
C-style array is not preferred, should use STD libraries.
* std::array
```cpp
array<int, 3> arr = {9, 8, 7};
cout << "Array size = " << arr.size() << endl;
cout << "2nd element = " << arr[1] <<endl;
```
**NOTE** both C-style and STD libraries ARRAYs have a fixed size, which
should be known at compilation time.


## C++17 Syntaxes
* If initializer allows user to include an initializer inside an if statement using the following syntax
```cpp
if (<initializer>; <conditional_expression>) {<body>}
```
where any variables introduced in this is only avaialble to conditional_expression and body.

* Similar to if initializer C++17 also allows initializer in switch
```cpp
switch(<initializer>; <expression>) { <body> }
```

* use auto to figure out return type of a function automatically
```cpp
auto addNumbes(int number1, int number2)
{
    return number1 + number2;
}
```

* Similar to python code like
```python
a, b = (1, 2)
```
C++17 now also supports structured bindings
```cpp
struct Point{ double mx, my, mz;};
Point point;
point.mx=1.0; point.my = 2.0; point.mz = 3.0;
auto [x, y, z] = point; // Here x, y, z will get the values from point
```
fLyMd-mAkEr


