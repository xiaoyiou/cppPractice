# Notes for C++ syntax and C++17
Using this note to track down the missing knowledge for C++ in the following aspects
1. Basic C++ syntax recap
2. C++17 special syntax and extension
3. OOP related special details

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
