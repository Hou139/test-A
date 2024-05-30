C_note

## Logical Operators

If you are checking to see if two or more parts are true you can use && between them. If you want to see if any of the parts is true you can use ||. To see both in action here is a trivial example:

```
int a = 2;
int b = 3;
if (a == b && a == 2) {
  printf("both are true\n");
}
if (a == b || a == 2) {
  printf("one or both are true\n");
}
if (!(a == b)) {
  printf("they are not equal\n");
}
```

## Arrays 

An array is a grouping of variables of the same type into contiguous blocks of memory.
There are two types of arrays that can be created: an initialized array or an uninitialized array. As its name implies, an uninitialized array is created without specifying the initial values it contains. 
```
int age[4];
```
To indicate to the compiler that age is an array of ints and not a single int variable, we append [arraySize] (in this case, arraySize is four) to the end of the variable name.
> dataType name[arraySize];

In contrast, an initialized array is created by specifying the initial value of its elements. As an example, we will create an age array with four initial ages:
>dataType name[] = {firstValue, secondValue, thirdValue, …};

## Array Access and Element Modification
-
Array elements can be accessed, modified, and used just like any other variable of the same data type. The following shows how to access an element in an array at index idx:

> arr[idx]

The first element in an array has index 0 and the last element in an array has index arraySize - 1. The nth element is at index n-1, so, for example, the third element would be at index 2.

An element in an array is modified just like a regular variable:

> arr[idx] = newValue

## Length of Array Using sizeof()

>sizeof(arr);

the sizeof() function can also be applied to any data type to determine its size in memory. The syntax is the same as that for an array:

>sizeof(dataType);
```
// Assign size of array to variable len. Scale by the size of an int.
int len = sizeof(arr)/sizeof(int);
```

## Multidimensional Arrays

``` 
int mat[3][4]; 
int mat2[][3] = {{1, 6, 3}, {5, 9, 2}};
```
## Looping Through Strings
To remedy this problem and make the loop valid for strings of any length, we can use the strlen() function. This function determines the length of the string. It is used like so:

>strlen(str)

The strlen() function is a special string function contained in the string library. To use it, the code must include the following line at the top of the file:

>#include<string.h>

## Concatenating Strings
``` 
strcat(dst, src);
```
At first glance, it may appear that some magic has taken place here because it is known that strings (because they are arrays) are immutable! What actually happens is the function takes the two strings and creates a char array of size strlen(src) +